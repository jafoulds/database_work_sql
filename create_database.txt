CREATE TABLE Classes (
	class CHAR(30),
	"type" CHAR(2),
	country CHAR(30),
	numGuns INT,
	bore INT,
	displacement INT
);

CREATE TABLE Ships (
	name CHAR(30),
	class CHAR(30),
	launched INT
);

CREATE TABLE Battles (
	name CHAR(30),
	date_fought DATE
);

CREATE TABLE Outcomes (
	ship CHAR(30),
	battle CHAR(30),
	"result" CHAR(20)
);

INSERT ALL
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Bismarck','bb','Germany',8,15,42000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Kongo','bc','Japan',8,14,32000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('North Carolina','bb','USA',9,16,37000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Renown','bc','Gt. Britain',6,15,32000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Revenge','bb','Gt. Britain',8,15,29000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Tennessee','bb','USA',12,14,32000)
INTO Classes (class, "type", country, numGuns, bore, displacement) VALUES
('Yamato','bb','Japan',9,18,65000)
SELECT * FROM dual;

For Ships

INSERT ALL
INTO Ships  VALUES ('California','Tennessee',1921)
INTO Ships VALUES ('Haruna','Kongo',1915)
INTO Ships VALUES ('Hiei','Kongo',1914)
INTO Ships VALUES ('Iowa','Iowa',1943)
INTO Ships VALUES ('Kirishima','Kongo',1914)
INTO Ships VALUES ('Kongo','Kongo',1913)
INTO Ships VALUES ('Missouri','Iowa',1944)
INTO Ships VALUES ('Musashi','Yamato',1942)
INTO Ships VALUES ('New Jersey','Iowa',1943)
INTO Ships VALUES ('North Carolina','North Carolina',1941)
INTO Ships VALUES ('Ramilles','Revenge',1917)
INTO Ships VALUES ('Renown','Renown',1916)
INTO Ships VALUES ('Repulse','Renown',1916)
INTO Ships VALUES ('Resolution','Revenge',1916)
INTO Ships VALUES ('Revenge','Revenge',1916)
INTO Ships VALUES ('Royal Oak','Revenge',1916)
INTO Ships VALUES ('Royal Sovereign','Revenge',1916)
INTO Ships VALUES ('Tennessee','Tennessee',1920)
INTO Ships VALUES ('Washington','North Carolina',1941)
INTO Ships VALUES ('Wisconsin','Iowa',1944)
INTO Ships VALUES ('Yamato','Yamato',1941)
SELECT * FROM dual;


INSERT ALL
INTO Battles VALUES  ('North Atlantic', TO_DATE ( '27-May-1941', 'DD-Mon-YYYY'))
INTO Battles VALUES  ('Guadalcanal', TO_DATE ('15-Nov-1942', 'DD-Mon-YYYY'))
INTO Battles VALUES  ('North Cape', TO_DATE ('26-Dec-1943', 'DD-Mon-YYYY'))
INTO Battles VALUES  ('Surigao Strait', TO_DATE ('25-Oct-1944', 'DD-Mon-YYYY'))
SELECT * FROM dual;



INSERT ALL
INTO Outcomes VALUES ('Bismarck','North Atlantic', 'sunk')
INTO Outcomes VALUES ('California','Surigao Strait', 'ok')
INTO Outcomes VALUES ('Duke of York','North Cape', 'ok')
INTO Outcomes VALUES ('Fuso','Surigao Strait', 'sunk')
INTO Outcomes VALUES ('Hood','North Atlantic', 'sunk')
INTO Outcomes VALUES ('King George V','North Atlantic', 'ok')
INTO Outcomes VALUES ('Kirishima','Guadalcanal', 'sunk')
INTO Outcomes VALUES ('Prince of Wales','North Atlantic', 'damaged')
INTO Outcomes VALUES ('Rodney','North Atlantic', 'ok')
INTO Outcomes VALUES ('Scharnhorst','North Cape', 'sunk')
INTO Outcomes VALUES ('South Dakota','Guadalcanal', 'ok')
INTO Outcomes VALUES ('West Virginia','Surigao Strait', 'ok')
INTO Outcomes VALUES ('Yamashiro','Surigao Strait', 'sunk')
SELECT * FROM dual;
