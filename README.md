# INDIAN_BANK-SQL
INDIAN  BANK SQL PROJECT 1


INDIAN BANK – CA SE STUDY
DATABASE DESIGN: 

1 . Create a DATABASE: INDIAN BANK 

2 . Create a secondary filegroup and assign a couple of files to it.

3 . Make the secondary filegroup as the default filegroup. 

4 . Create the below tables. Place them in different filegroups if they are  to be used in joins. 

TABLES: 

ACCOUNT MASTER 


|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|-----------------| 
|  ACID           |     INT           |  PK             |
|  NAME           |     VARCHAR(20)   |  NOT NULL       |
|  ADDRESS        |     VARCHAR(50)   |  NOT NULL       |
|  BRID           |     CHAR(3)       |   NOT NULL FK   |
|  PID            |     CHAR(2)       |   NOT NULL FK   |
|  DOO            |     DATETIME      |   NOT NULL      |
|  CBALANCE       |     MONEY         |    NULL         |
|  UNCBALANCE     |     MONEY         |     NULL        |
|  STATUSS        |     CHAR(1)       |  O’ for ‘OPERATIVE’, ‘I’ for ‘INOPERATIVE’, ‘C’ for ‘CLOSED’; NOT NULL; DEFAULT value is ‘O’ (OPERATIVE)| 


TABLE 2

PRODUCT MASTER 

|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|-----------------| 
|   PID           |   CHAR(2)         |   PK            |
|   PRODUCTNAME   |   VARCHAR(15)     |  NULL           |

TABLE 3

REGION MASTER


|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|-----------------| 
|     RID         |     INT           |   PK            |
|   REGIONNAME    |     CHAR(6)       |   NOT NULL      |

TABLE 4 

BRANCH MASTER

|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|-----------------| 
|   BRID          |     CHAR(3)       |   PK            |
| BRANCHNAME      | VARCHAR(30)       |   NOT NULL      |
| BRANCHADRESS    | VARCHAR(50)       |   NOT NULL      |
|   RID           | INT               |   FK NOT NULL   |

TABLE 5 
USERMASTER

|   COLUMN NAME   |     DATATYPE      |     REMARK      |
|-----------------|-------------------|-----------------| 
| USERID          |   INT             |   PK            |
| USERNAME        |   VARCHAR(30)     |   NOT NULL      |
| DESIGNATION     |   CHAR(1)         |  M’ for ‘MANAGER’, ‘T’ for ‘TELLER’, ‘C’ for CLERK NOT NULL |


TABLE 6

TRANSACTION MASTER

|   COLUMN NAME   |     DATATYPE      |     REMARK                    |
|-----------------|-------------------|-------------------------------| 
| TRANNO          |     INT           | PK IDENTITY SEED 1 INCREMENT 1|
| DOT             |   DATETIME        |   NOT NULL                    |
| ACID            |   INT             | FK NOT NULL                   |
|  BRID           | CHAR(3)           | FK NOT NULL                   |
|  TXN_TYPE       |   CHAR(3)         |CW’ for ‘CASH WITHDRAWAL’, ‘CD’ for ‘CASH DEPOSIT’, ‘CQD’ for ‘CHEQUE DEPOSIT’; NOT NULL |
| CHQ_NO          |  INT              |   NULL                        | 
|CHQ_DATE         | SMALL datetime    |  null                         |
|TXN_ACCOUNT      |  money            |   not null                    |
| userid          |  int              |     fk not null               |
