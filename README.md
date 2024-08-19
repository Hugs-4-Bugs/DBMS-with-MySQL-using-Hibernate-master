
# DBMS with MySQL using Hibernate


In this project, I have worked on Database Management in MySQL using Advanced Concepts of Hibernate JAVA in Eclipse.
This project demonstrates a simple Database Management System (DBMS) using MySQL and Hibernate.

## Project Structure

The repository includes the following directories:

- **basic**: Contains basic Hibernate configuration and usage examples.
- **hb-01-one-to-one-uni**: Demonstrates a one-to-one unidirectional mapping.
- **hb-02-one-to-one-bi**: Demonstrates a one-to-one bidirectional mapping.
- **hb-03-one-to-many**: Demonstrates a one-to-many bidirectional mapping.
- **hb-04-one-to-many-uni**: Demonstrates a one-to-many unidirectional mapping.
- **hb-05-many-to-many**: Demonstrates a many-to-many bidirectional mapping.
- **hb-eager-vs-lazy-demo**: Shows the difference between eager and lazy loading in Hibernate.
- **Hibernate Database Scripts**: Contains SQL scripts for setting up and populating the database.

## Cloning the Repository

To clone this repository, use the following command:

```bash
git clone https://github.com/Hugs-4-Bugs/DBMS-with-MySQL-using-Hibernate-master.git
```

### Downloading the Repository

Alternatively, you can download the repository as a ZIP file by clicking on the "Code" button on the GitHub repository page and selecting "Download ZIP".

## Running the Project

### Prerequisites

- **Java**: Version 8 or higher
- **MySQL**: Version 8 or higher
- **Hibernate**: Version 5 or higher
- **IDE**: Eclipse or any other Java-based IDE (optional)

### Setting up the Project

1. **Import the project** into your preferred IDE (e.g., Eclipse) or create a new Java project and add the cloned/downloaded files to it.

2. **Configure the MySQL database connection** by creating a `hibernate.cfg.xml` file with the following contents:

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <!DOCTYPE hibernate-configuration PUBLIC
            "-//Hibernate/Hibernate Configuration DTD 3.0//EN"
            "http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">
    
    <hibernate-configuration>
        <session-factory>
            <property name="connection.url">jdbc:mysql://localhost:3306/mydb</property>
            <property name="connection.username">your_username</property>
            <property name="connection.password">your_password</property>
            <property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>
            <property name="hibernate.show_sql">true</property>
            <property name="hibernate.hbm2ddl.auto">update</property>
        </session-factory>
    </hibernate-configuration>
    ```

    Replace `your_username`, `your_password`, and `mydb` with your actual MySQL credentials and database name.

3. **Create the necessary database schema** by running the following command:

    ```bash
    mysql -u your_username -p your_password < create_database.sql
    ```

    Replace `your_username`, `your_password`, and `create_database.sql` with your actual MySQL credentials and the SQL file provided in the repository.

### Running the Application

1. **Compile the Java files** using your preferred IDE or by running the following command:

    ```bash
    javac -cp .;hibernate-release-5.4.20.Final/lib/* Main.java
    ```

2. **Run the application** using the following command:

    ```bash
    java -cp .;hibernate-release-5.4.20.Final/lib/* Main
    ```

    This will execute the `Main` class, which demonstrates the CRUD (Create, Read, Update, Delete) operations using Hibernate.

## Troubleshooting

If you encounter any issues while running the project, check the following:

- Ensure that you have the correct MySQL credentials and database name in the `hibernate.cfg.xml` file.
- Verify that the MySQL database is running and accessible.
- Check the Hibernate configuration and dependencies.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository, make your changes, and submit a pull request.

## Author

[Hugs-4-Bugs](https://github.com/Hugs-4-Bugs)
