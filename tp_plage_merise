#------------------------------------------------------------
#        Script MySQL.
#------------------------------------------------------------


#------------------------------------------------------------
# Table: region
#------------------------------------------------------------

CREATE TABLE region(
        id_region          Int  Auto_increment  NOT NULL ,
        nom_responsable    Varchar (35) NOT NULL ,
        prenom_responsable Varchar (35) NOT NULL ,
        nom_region         Varchar (35) NOT NULL
	,CONSTRAINT region_PK PRIMARY KEY (id_region)
)ENGINE=InnoDB;


#------------------------------------------------------------
# Table: dept
#------------------------------------------------------------

CREATE TABLE dept(
        id_dept         Int  Auto_increment  NOT NULL ,
        nom_departement Varchar (35) NOT NULL ,
        id_region       Int NOT NULL
	,CONSTRAINT dept_PK PRIMARY KEY (id_dept)

	,CONSTRAINT dept_region_FK FOREIGN KEY (id_region) REFERENCES region(id_region)
)ENGINE=InnoDB;


#------------------------------------------------------------
# Table: ville
#------------------------------------------------------------

CREATE TABLE ville(
        id_ville     Int  Auto_increment  NOT NULL ,
        nom_ville    Varchar (35) NOT NULL ,
        code_postal  Int NOT NULL ,
        nbr_touriste Int NOT NULL ,
        id_dept      Int NOT NULL
	,CONSTRAINT ville_PK PRIMARY KEY (id_ville)

	,CONSTRAINT ville_dept_FK FOREIGN KEY (id_dept) REFERENCES dept(id_dept)
)ENGINE=InnoDB;


#------------------------------------------------------------
# Table: plage
#------------------------------------------------------------

CREATE TABLE plage(
        id_plage   Int NOT NULL ,
        long_plage Int NOT NULL ,
        type_plage Varchar (35) NOT NULL ,
        id_ville   Int NOT NULL
	,CONSTRAINT plage_PK PRIMARY KEY (id_plage)

	,CONSTRAINT plage_ville_FK FOREIGN KEY (id_ville) REFERENCES ville(id_ville)
)ENGINE=InnoDB;

