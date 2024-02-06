
# Exploring Real-Time Data Processing: with AWS, Docker, NiFi, and Snowflake"

In this project, I developed an automated real-time data streaming pipeline to orchestrate the flow of data using modern technologies. 

The goal was to build a smart system capable of swiftly processing real-time data and storing it in an AWS S3 storage space. The entire data flow is automated using pipelines and continuous integration. The system further processes this data in real-time using Snowflake, all managed by Apache NiFi.





## Architecture Flow

![App Screenshot](https://github.com/VennapusaManoj1998/Developing-Real-Time-Data-Processing-with-AWS-Docker-NiFi-and-Snowflake./blob/main/Workflow.jpeg)


## Key Components


- **Apache NiFi:** Orchestrates the real-time flow of data, ensuring seamless integration and processing.

- **AWS S3:** Provides scalable storage for the streamed data, enabling real-time access and storage.

- **Snowflake:** Processes the data in real-time, leveraging Snowpipe for automatic data ingestion and processing.

- **AWS EC2:** Hosts the entire system, providing the infrastructure for deployment and execution.

- **IAM (Identity and Access Management):** Manages permissions and access control for AWS services, ensuring secure and controlled data processing.


## Project Setup

- Configured an AWS EC2 instance with specific requirements for optimal performance.
- Set up a Docker container containing Python, Apache NiFi, and Apache ZooKeeper within the EC2 instance.
- Configured JupyterLab and Apache NiFi to run on specific ports for data processing and orchestration.
- Used Python in JupyterLab to generate random data records, simulating customer information.
- Utilized Apache NiFi to transfer the generated data to an AWS S3 bucket for scalable storage and real-time access.
- Leveraged Snowpipe, Snowflake streams, and tasks for real-time data processing and automatic updates.
## Project 

**Data Generation with Faker Python Library**

The project began with the generation of synthetic data using the Faker Python library. This simulated data served as a testbed for evaluating our real-time processing capabilities.

**Real-Time Processing with NiFi**

Our data underwent real-time ingestion and transformation in Apache NiFi. NiFi was configured to connect to the Faker data source, and the processed data was efficiently written to an S3 bucket in CSV format. This S3 bucket served as a staging area before the data was loaded into Snowflake.

**AWS EC2 Instance and Docker Compose**

The entire system was hosted on an AWS EC2 instance, leveraging Docker for containerization. Docker Compose orchestrated the deployment of Zookeeper, NiFi, and other essential components, simplifying the setup process.

**Snowflake Integration for Data Warehousing**

Snowflake, a cloud-based data warehousing platform, was used to store and manage our processed data. Snowpipe, Snowflake's data ingestion service, handled delta loading into the customer_raw staging table, acting as the gateway to our structured data.

**Slowly Changing Dimension (SCD) Type 1 (SCD-1)**

In SCD-1, the production table (customer) maintained only the latest version of each record without historical tracking. This approach allowed us to capture the current state of data without retaining historical changes.


## Key Achievements

- Demonstrated the ability to design and implement a real-time data streaming pipeline using modern technologies.
- Showcased proficiency in cloud computing, data warehousing, and real-time data processing.
- Highlighted expertise in Apache NiFi, AWS, Snowflake, and Python for data engineering and automation.

**This project exemplifies my skills in developing robust and scalable data pipelines for real-time data processing, enabling efficient data analysis and decision-making.**



