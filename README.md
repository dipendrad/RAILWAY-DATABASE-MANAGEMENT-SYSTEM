# RAILWAY-DATABASE-MANAGEMENT-SYSTEM
This project aims to analyze railway passenger data and reservation details to derive meaningful insights. The dataset consists of two tables: passenger and reservation. Various SQL queries are used to perform analyses, such as identifying popular destinations, revenue generation, payment modes, and class preferences.

# Project Structure
- Database Creation and Data Insertion: SQL scripts to create and populate the passenger and reservation tables.
- Analysis Queries: SQL queries to analyze the data.
# README.md: Detailed project documentation.
- Database Schema
- Passenger Table
- pid: INT(10), unique, not null - Passenger ID
- tid: INT(10), primary key - Ticket ID
- pname: VARCHAR(30) - Passenger Name
- ticketfare: INT(10) - Ticket Fare
- paymentmode: VARCHAR(30) - Payment Mode
- destination: VARCHAR(30) - Destination
