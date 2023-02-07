# INDIAN_BANK-SQL
INDIAN  BANK SQL PROJECT 1


INDIAN BANK – CA SE STUDY
DATABASE DESIGN: 
1 . Create a DATABASE: INDIAN BANK 

2 . Create a secondary filegroup and assign a couple of files to it.

3 . Make the secondary filegroup as the default filegroup. 
4 . Create the below tables. Place them in different filegroups if they are 
to be used in joins. 
TABLES: 
ACCOUNT MASTER 

|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|  PRIMARY KEY    |
|  ACID           |     INT           |  NOT NULL       |
|  NAME           |     VARCHAR(20)   |  NOT NULL       |
|  ADDRESS        |     VARCHAR(50)   |  NOT NULL       |
|  BRID           |     CHAR(3)       |   NOT NULL FK   |
|  PID            |     CHAR(2)       |   NOT NULL FK   |
|  DOO            |     DATETIME      |   NOT NULL      |
|  CBALANCE       |     MONEY         |    NULL         |
|  UNCBALANCE     |     MONEY         |     NULL        |
|  STATUSS        |     CHAR(1)       |      O’ for ‘OPERATIVE’, ‘I’ for ‘INOPERATIVE’, ‘C’ for ‘CLOSED’; NOT NULL; DEFAULT value is ‘O’ (OPERATIVE) |
