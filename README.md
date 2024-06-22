# RAILWAY-DATABASE-MANAGEMENT-SYSTEM
use railwaydatabase;

create table passenger(pid int(10) unique not null,tid int(10) primary key,pname varchar(30),ticketfare int(10),paymentmode varchar(30),destination varchar(30));

insert into passenger values(701,1001,'sachin',1200,'debitcard','Mumbai'),(702,1002,'Rahul',1120,'Creditcard','Delhi'),(703,1003,'Saurav',1300,'UPI','Pune'),(704,1004,'Anil',1280,'debitcard','Delhi'),(705,1005,'Ramesh',1400,'Netbanking','Mumbai'),(706,1006,'John',1120,'Creditcard','Pune'),(707,1007,'Sujit',1400,'UPI','Mumbai'),(708,1008,'Vishal',1280,'Netbanking','Delhi'),(709,1009,'Yash',1170,'Creditcard','Nashik'),(710,1010,'Rohit',1300,'UPI','Nagpur'),(711,1011,'Rupesh','1400','Netbanking','Nashik'),(712,1012,'Aman',1480,'UPI','Kolkata');

select * from passenger;

select COUNT(*)  FROM passenger;

select pid,tid, pname ,ticketfare  from passenger where ticketfare = (select max(ticketfare) from passenger); 

select pname ,ticketfare ,tid from passenger where ticketfare = (select min(ticketfare) from passenger);

select count(pname) from passenger where destination = 'Mumbai';

select avg(ticketfare) from passenger;

select SUM(ticketfare) FROM passenger;

select destination, COUNT(*) FROM passenger GROUP BY destination;

select paymentmode, SUM(ticketfare) FROM passenger GROUP BY paymentmode;

SELECT paymentmode, COUNT(*) FROM passenger GROUP BY paymentmode;

select pname FROM passenger WHERE destination = 'Delhi';

select destination, SUM(ticketfare) FROM passenger GROUP BY destination ORDER BY destination asc;
create table reservation (pid int(10), class varchar(30), Dateofjourney date);
insert into reservation values(700,'AC1','2023-04-14'),(702,'SC','2023-05-04'),(701,'AC1','2023-04-12'),(703,'AC2','2023-04-14'),(705,'AC2','2023-04-15'),(706,'AC1','2023-04-17'),(707,'SC','2023-04-15'),(711,'AC2','2023-04-19'),(712,'AC1','2023-04-01'),(707,'SC','2023-04-09'),(709,'AC1','2023-04-02'),(710,'SC','2023-04-06'),(711,'AC2','2023-04-11'),(704,'SC','2023-04-09');
select * from reservation;

SELECT class, COUNT(*) FROM reservation GROUP BY class;

SELECT r.class, SUM(p.ticketfare) AS total_revenue 
FROM reservation r 
JOIN passenger p ON r.pid = p.pid 
GROUP BY r.class;

SELECT p.pname, r.Dateofjourney 
FROM passenger p 
JOIN reservation r ON p.pid = r.pid 
WHERE r.class = 'AC1';

SELECT p.pid, p.pname, p.ticketfare, r.class, r.Dateofjourney
FROM passenger p
INNER JOIN reservation r ON p.pid = r.pid;

SELECT p.pid, p.pname, p.ticketfare, r.class, r.Dateofjourney
FROM passenger p
LEFT JOIN reservation r ON p.pid = r.pid;

SELECT p.pid, p.pname, p.ticketfare, r.class, r.Dateofjourney
FROM passenger p
RIGHT JOIN reservation r ON p.pid = r.pid;









