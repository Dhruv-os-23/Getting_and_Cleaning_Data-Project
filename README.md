**Coursera Getting and Cleaning Data Course Project**

*Overview:*
Wearable computing is a rapidly evolving field, with companies like Fitbit, Nike, and Jawbone Up competing to develop advanced algorithms that engage users. In this project, we retrieved, processed, and cleaned data collected from the accelerometer and gyroscope of a Samsung Galaxy S smartphone, creating a tidy dataset suitable for analysis.

*Repository Contents:*
1. **README.md:** Provides an overview of the dataset's creation and content.
2. **tidy_data.txt:** Contains the final, cleaned dataset.
3. **CodeBook.md:** Describes the data, variables, and transformations used.
4. **run_analysis.R:** The R script that created the dataset.

*Study Design:*
The source data comes from the "Human Activity Recognition Using Smartphones" dataset, describing data collection as follows:
- 30 volunteers aged 19-48 performed six activities while wearing a smartphone.
- The smartphone's accelerometer and gyroscope captured 3-axial linear acceleration and angular velocity at 50Hz.
- Data was partitioned into training (70% of volunteers) and test (30% of volunteers) sets.
- Sensor signals underwent pre-processing, filtering, and feature extraction.

*Creating the Data Set:*
The R script, "run_analysis.R," was used to create the dataset, implementing the following steps:

1. Download and unzip source data if not already available.
2. Read the data.
3. Merge training and test sets into a unified dataset.
4. Extract mean and standard deviation measurements for each variable.
5. Use descriptive activity names to label activities.
6. Assign descriptive variable names to the dataset.
7. Create an independent tidy dataset with the average of each variable for each activity and subject.
8. Write the tidy dataset to "tidy_data.txt."

The "tidy_data.txt" was generated using R version 3.2.2 on Windows 8.1 (64-bit) and required the dplyr package (version 0.4.3).

*Summary:*
This project demonstrates the process of collecting, cleaning, and transforming raw sensor data into a tidy dataset suitable for analysis. The resulting dataset is structured, well-documented, and ready for use in data science and wearable computing applications.
