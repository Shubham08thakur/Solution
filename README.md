# Exercise 1

Automated Testing Script for Kloudship Application
This script is designed to automate the testing of certain functionalities within the Kloudship application using Selenium WebDriver. Kloudship is an application that presumably deals with shipping logistics.

# Exercise 2
-- SELECT the details of Doctor(s) who has got Admissions.
SELECT DISTINCT d.doctor_id, d.first_name, d.last_name, d.specialty
FROM Doctors d
JOIN Admissions a ON d.doctor_id = a.attending_doctor_id;


-- SELECT the details of Doctor(s) for whom there is no Admissions.
SELECT d.doctor_id, d.first_name, d.last_name, d.specialty
FROM Doctors d
LEFT JOIN Admissions a ON d.doctor_id = a.attending_doctor_id
WHERE a.attending_doctor_id IS NULL;


-- SELECT the details of Patient(s) whose Admission can’t be completed due to missing doctor details
SELECT p.patient_id, p.first_name, p.last_name, p.gender, p.birth_date, p.city, p.province_id, p.allergies, p.height, p.weight
FROM Patients p
LEFT JOIN Admissions a ON p.patient_id = a.patient_id
WHERE a.attending_doctor_id IS NULL;

# Exercise 3

SQL Solution for Doctor and Patient Admission Details
This repository contains SQL queries to extract details about doctors, patients, and their admissions from a database. Below are the descriptions of each query and their purpose.

Doctors with Admissions Purpose: Retrieves details of doctors who have admissions associated with them.

Doctors without Admissions Purpose: Retrieves details of doctors who do not have any admissions associated with them.

Patients with Incomplete Admissions Purpose: Retrieves details of patients whose admissions cannot be completed due to missing doctor details.

How to Use Ensure you have access to the database containing the required tables (Doctors, Admissions, Patients). Copy and paste the queries into your SQL client or database management system. Execute the queries to retrieve the desired information.
