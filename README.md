create table Patients(PatientID varchar(255) PRIMARY KEY,
PatientName varchar(255),
Gender varchar(255),
DateofBirth Date,
Contacts varchar(255));

insert into Patients values
("P001","Leonard Odipo","Male","1-04-1987","0782789876"),
("P002","Margret Kingori","Female","7-10-1964","0734762891"),
("P003","Femi Njeri","Female","9-03-2007","0746839229"),
("P004","Emmanuel Mutua","Male","1-04-1999","0112399203"),
("P005","Fred Nganga","Male","10-10-1990","0722354765"),
("P006","Mary Nyanchama","Female","4-06-1980","0790876563"),
("P007","Donold Wangui","Male","8-05-2000","0743788729"),
("P008","Imani Atieno","Female","9-07-1993","0737419493"),
("P009","Natalie Rose","Female","7-09-2003","0783013130"),
("P010","David Bonte","Male","4-08-2005","0152219020");


create table Immunization(ImmunizationId varchar(255) PRIMARY KEY,
VaccineName varchar(255),
Dateimmunized Date,
FOREIGN KEY (PatientID)REFERENCES Patients(PatientID));

insert into Immunization values
("I001","Polio","9-07-1992","P001"),
("I002","BCG","6-08-1971","P002"),
("I003","Whooping Cough","9-09-1997","P003"),
("I004","COVID-19","10-07-2022","P004"),
("I005","BCG","4-03-1998","P005"),
("I006","Tetenus","6-12-1985","P006"),
("I007","Yellow-Fever","30-06-2017","P007"),
("I008","Polio","16-11-1998","P008"),
("I009","Whooping Cough","7-09-2003","P009"),
("I010","COVID-19","30-04-2021","P010");
