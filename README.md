# e_t-caret-diyagram

create database E_TİCARET

create table ORDERS(
ID int identity(1,1) not null primary key,
USERID int not null,
DATETIME_ int not null,
TOTALPRICE int not null,
STATUS_ nvarchar(50),
ADRESSID_ int
);

create table ORDERDETAILS(
ID int identity(1,1) not null primary key,
ORDERID int not null,
ITEMID int not null,
AMOUNT int not null,
UNITPRICE varchar(50) not null,
LINETOTAL varchar(50) not null,
foreign key (ORDERID) references ORDERS(ID)
);

create table ADRESS(
ID int identity(1,1) not null primary key,
USERID int not null,
COUNTRYID int not null,
CITYID int not null,
TOWNID int not null,
DISTRICTID int not null,
POSTALCODE varchar(50),
ADRESSTEXT varchar(50)
);
