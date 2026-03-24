CREATE TABLE customer_location AS
SELECT
    location.location_id,
    location.state,
    customer.customer_id,
    customer.monthly_charge
FROM
    location
JOIN
    customer ON location.location_id = customer.location_id;
	
CREATE TABLE avg_monthly_state AS
SELECT
    state,
    AVG(customer_location.monthly_charge) AS average_monthly_charges
FROM
    customer_location
GROUP BY
    state
ORDER BY
    state ASC;
	
ALTER TABLE aggregated_churn_data
ADD COLUMN total_customers INT;

UPDATE aggregated_churn_data
SET total_customers = (SELECT COUNT(*) FROM customer_location WHERE state = aggregated_churn_data.state);

ALTER TABLE aggregated_churn_data
ADD COLUMN customer_id INT;

UPDATE aggregated_churn_data
SET total_customers = (SELECT COUNT(*) FROM customer_location WHERE state = aggregated_churn_data.state);
SELECT *
FROM aggregated_churn_data
Limit 10;
