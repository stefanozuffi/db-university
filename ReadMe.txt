Departments: 
- id INT || BIGINT NOTNULL UNIQUE
- departmentID SMALL NOTNULL UNIQUE
- name VARCHAR(75) NOTNULL
- location VARCHAR(?) [depends on the university's nomenclature system]


Degrees:
- id INT || BIGINT NOTNULL UNIQUE
- dep_id 
- name VARCHAR(75) NOTNULL 
- subject_type VARCHAR(50) 
- credits TINYINT || SMALL NOTNULL
- available_pt TINYINT
- has_admission_requirements TINYINT
- max_capacity SMALL
- num_students SMALL NOTNULL

Courses: 
- id INT || BIGINT NOTNULL UNIQUE 
- courseID MEDIUM NOTNULL UNIQUE
- credits TINYINT NOTNULL
- name VARCHAR(75) NOTNULL 
- has_prerequisites TINYINT 
- max_capacity SMALL
- num_students SMALL

Teachers:
- id INT || BIGINT NOTNULL UNIQUE
- teacherID MEDIUM NOTNULL UNIQUE
- fullName VARCHAR(150)
- date_of_birth DATE
- place_of_birth VARCHAR(150)
- residence VARCHAR(150)
- department_id 
 

Students: 
- id INT || BIGINT NOTNULL UNIQUE
- studentID INT NOTNULL UNIQUE
- fullName VARCHAR(150)
- date_of_birth DATE
- place_of_birth VARCHAR(150)
- residence VARCHAR(150) 
- gpa TINYINT
- perc_attendance FLOAT(4,3)


Exams: 
- id INT || BIGINT NOTNULL UNIQUE
- course_id 
- date DATE
- time TIME
- place VARCHAR(150)
- credits_worth TINYINT NOTNULL 