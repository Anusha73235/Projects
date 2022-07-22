--BANK DATABASE
--CUSTOMER PERSONAL INFORMATION

CREATE TABLE CUSTOMER(ID INT,C_NAME VARCHAR2(50),DOB DATE, CONTACT_NO INT,ADDRESS VARCHAR2(100),GENDER CHAR(5),MAIL_ID VARCHAR2(50),
MARTIVAL_STATUS  VARCHAR2(10), CONSTRAINT CUST_INFO PRIMARY KEY(ID));

-- CUSTOMER REFERENCE INFORMATION
CREATE TABLE CUSTOMER_INFO(ID INT,ACC_NAME VARCHAR2(20),ACC_NO VARCHAR2(16),ACC_ADDRESS VARCHAR2(25),
CONSTRAINT CUST_REF_INFO PRIMARY KEY(ID),FOREIGN KEY(ID) REFERENCES CUSTOMER(ID));

-- BANK INFORAMTION

CREATE TABLE BANK_INFO(IFSC_CODE VARCHAR2(15),BANK_NAME VARCHAR2(25),
BRANCH_NAME VARCHAR2(25),CONSTRAINT BANK_INFO_PK PRIMARY KEY(IFSC_CODE));

--INSERTING VALUES

INSERT INTO CUSTOMER VALUES(1, 'SAHIL', '04-06-1998', '987654321', 'JALANDHAR', 'M', 'SAHILKALYAN@GMAIL.COM', 'SINGLE');
INSERT INTO CUSTOMER VALUES(2, 'HARPREET', '31-10-1978', '986532741', 'LAXMI NAGAR, DELHI', 'M', 'HAPPYSINGH@GMAIL.COM', 'SINGLE');
INSERT INTO CUSTOMER VALUES(3,'NEELIMA','11-09-1786','9087654321','RAJESWARI NAGAR,NELLORE','F','NEEL123@GMAIL.COM','SINGLE');
INSERT INTO CUSTOMER VALUES(4,'AKBAR','18-09-1893','7345678901','NADYALA','M','AKBAR126@GMAIL.COM','SINGLE');
INSERT INTO CUSTOMER VALUES(5,'NEELAVENI','06-09-1987','9876543217','KAMALAPURAM','F','NEELIOPU7323@GMAIL.COM','MARRIED');
INSERT INTO CUSTOMER VALUES(6,'KALYAN','08-06-1997','8765432190','TIRUPATI','M','KALYAN09@GMAIL.COM','SINGLE');
INSERT INTO CUSTOMER VALUES(7,'BHARGAVI','09-11-1996','9134567812','NELLORE','F','BHAR5342@GMAIL.COM','SINGLE');
INSERT INTO CUSTOMER VALUES(8,'UMA','05-08-1994','8698764521','MRPALLI','F','UMA234@GMAIL.COM','SINGLE');
INSERT INTO CUSTOMER VALUES(9,'SATHISH','28-03-1990','8497923678','MUIKIRNAGAR','M','IUOP89@GMAIL.COM','MARRIED');
INSERT INTO CUSTOMER VALUES(10,'ILIYAS','09-02-1997','6347241256','RAJPALEM','M','TYPALI34@GMAIL.COM','SINGLE');
SELECT * FROM CUSTOMER ORDER BY ID ASC ;

INSERT INTO CUSTOMER_INFO VALUES(1, 'SAHIL', '12345678912', 'JALANDHAR, PUNJAB');
INSERT INTO CUSTOMER_INFO VALUES(2, 'HARPREET', '85236974123', 'LAXMI NAGAR, DELHI');
INSERT INTO CUSTOMER_INFO VALUES(3,'NEELIMA','61893567281','RAJESWARI NAGAR,NELLORE');
INSERT INTO CUSTOMER_INFO VALUES(4,'AKBAR','34567891235','NADYALA');
INSERT INTO CUSTOMER_INFO VALUES(5,'NEELAVENI','34215634578','KAMALAPURAM');
INSERT INTO CUSTOMER_INFO VALUES(6,'KALAYAN','76432153289','TIRUPATI');
INSERT INTO CUSTOMER_INFO VALUES(7,'BHARGAVI','54378231234','NELLORE');
INSERT INTO CUSTOMER_INFO VALUES(8,'UMA','45328974321','MRPALLI');
INSERT INTO CUSTOMER_INFO VALUES(9,'SATHISH','65782314578','MUIKIRNAGAR');
INSERT INTO CUSTOMER_INFO VALUES(10,'ILIYAS','45390008732','RAJPALAM');

SELECT * FROM CUSTOMER_INFO;

INSERT INTO BANK_INFO VALUES('SBI00040N', 'STATE BANK OF INDIA', 'SBI JANDHAR PUNJAB');
INSERT INTO BANK_INFO VALUES('PNB00P50', 'PUNJAB NATIONAL BANK', ' PNB LAXMI NAGAR DELHI');
INSERT INTO BANK_INFO VALUES('ICIC0075','ICIC BANK','ICIC NELLORE');
INSERT INTO BANK_INFO VALUES('SBI0080N','STATE BANK OF INDIA','SBI NADYALA');
INSERT INTO BANK_INFO VALUES('SBI00502','STATE BANK OF INDIA','SBI KAMALAPURAM');
INSERT INTO BANK_INFO VALUES('SBI00403','STATE BANK OF INDIA','SBI TIRUPATI');
INSERT INTO BANK_INFO VALUES('SBI00605','STATE BANK OF INDIA','SBI NELLORE');
INSERT INTO BANK_INFO VALUES('SBI00301','STATE BANK OF INDIA','SBI MRPALLI');
INSERT INTO BANK_INFO VALUES('SBI00902','STATE BANK OF INDIA','SBI MUIKINAGAR');
INSERT INTO BANK_INFO VALUES('PNB00P79','PUNJAB NATIONAL BANK', ' PNB RAJPALAM');

SELECT * FROM BANK_INFO;
