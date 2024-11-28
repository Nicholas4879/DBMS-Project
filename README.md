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

create table GrowthMetrics(MeasureId varchar(255) PRIMARY KEY,
Height(m) numeric(10,2),
Weight(Kg) int,
BMI int,
Date Date,
FOREIGN KEY (PatientID)REFERENCES Patients(PatientID));

insert into GrowthMetrics values
("M001", 1.67, 90, 31, "04-09-2000", "P001"),
("M002", 1.75, 85, 28, "23-03-1998", "P002"),
("M003", 1.60, 70, 27, "09-06-2005", "P003"),
("M004", 1.80, 95, 29, "19-02-1987", "P004"),
("M005", 1.65, 65, 24, "11-11-2010", "P005"),
("M006", 1.73, 78, 26, "29-01-2014", "P006"),
("M007", 1.68, 82, 29, "03-02-1993", "P007"),
("M008", 1.82, 88, 27, "15-10-2000", "P008"),
("M009", 1.70, 76, 26, "22-04-2002", "P009"),
("M010", 1.78, 92, 29, "31-12-2017", "P010");


create table AntenatalVisits(VisitID varchar(255) PRIMARY KEY,
DateofVisit Date,
HealthStatus varchar(255),
BloodPressure(mmHg) int,
Weight(Kg) int,
FOREIGN KEY (PatientID)REFERENCES Patients(PatientID));

insert into AntenatalVisits values
("V001", "23-12-2003", "Healthy", 90, 95, "P001"),
("V002", "11-10-1999", "Ailing", 60, 60, "P002"),
("V003", "01-04-2010", "Healthy", 85, 78, "P003"),
("V004", "15-02-2018", "Ailing", 70, 65, "P004"),
("V005", "02-07-1995", "Stable", 88, 85, "P005"),
("V006", "19-08-2007", "Healthy", 92, 90, "P006"),
("V007", "22-12-2000", "Ailing", 55, 50, "P007"),
("V008", "30-11-2006", "Stable", 80, 76, "P008"),
("V009", "05-09-2009", "Healthy", 95, 100, "P009"),
("V010", "08-07-2020", "Ailing", 65, 55, "P010");
