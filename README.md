Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:

- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.

Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

Utilizzare https://www.drawio.com/ per la creazione dello schema.
Esportare quindi il diagramma in png, caricarlo in un file html e pushare tutto nella repo.

# Table: departments

- id
- name
- type_departments
- phone
- email

# Table: degrees

- id
- department_id
- name
- app

# Table: courses

- id
- name
- app

# Table: teachers

- id
- name
- lastname
- phone
- email

## Pivot Table: course_teacher

- id
- course_id
- teacher_id

# Table: student

- id
- degree_id
- name
- lastname
- phone
- email

# Table: exams

- id
- course_id
- data
- start_time

## Pivot Table exam_student

- id 
- exam_id
- student_id
- vote