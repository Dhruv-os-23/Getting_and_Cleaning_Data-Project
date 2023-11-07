**Code Book for Coursera Getting and Cleaning Data Course Project**

This code book pertains to the "tidy_data.txt" dataset, which is the result of processing and cleaning data from accelerometers in the Samsung Galaxy S smartphone. The dataset consists of space-separated values, where the first row contains variable names, and subsequent rows contain corresponding values.

**Variables**

The dataset includes the following variables:

1. **Subject** (Identifier): An integer ranging from 1 to 30, representing the subject who participated in the study.

2. **Activity** (Identifier): A string with six possible values, denoting the activity the subject was engaged in. Possible activities include:
   - WALKING: Subject was walking
   - WALKING_UPSTAIRS: Subject was walking upstairs
   - WALKING_DOWNSTAIRS: Subject was walking downstairs
   - SITTING: Subject was sitting
   - STANDING: Subject was standing
   - LAYING: Subject was laying

3. **Average of Measurements**: The dataset contains 79 averaged signal measurements, which are all floating-point values normalized and bounded within [-1, 1]. The measurements are classified into two domains:

   **Time-Domain Signals**: These are results of capturing raw accelerometer and gyroscope signals and include the following categories:
   - Body Acceleration (in X, Y, and Z directions)
   - Gravity Acceleration (in X, Y, and Z directions)
   - Body Acceleration Jerk (derivative of acceleration)
   - Body Angular Velocity (in X, Y, and Z directions)
   - Body Angular Velocity Jerk (derivative of angular velocity)
   - Magnitude (of acceleration, gravity acceleration, acceleration jerk, angular velocity, and angular velocity jerk)

   **Frequency-Domain Signals**: These are obtained using the Fast Fourier Transform (FFT) on some of the time-domain signals and include the following categories:
   - Body Acceleration (in X, Y, and Z directions)
   - Body Acceleration Jerk (derivative of acceleration)
   - Body Angular Velocity (in X, Y, and Z directions)
   - Magnitude (of body acceleration, acceleration jerk, body angular velocity, and angular velocity jerk)

For each of the above categories, the dataset includes the following measurements:
- Mean
- Standard Deviation
- Mean Frequency (for frequency-domain signals)

**Transformations**

The dataset was derived from the source data by applying the following transformations:

1. Merging Training and Test Sets: The training and test datasets were combined to create a unified dataset.

2. Extracting Mean and Standard Deviation Measurements: Only the measurements related to mean and standard deviation were retained, and other measurements were discarded.

3. Descriptive Activity Names: Numeric activity codes were replaced with descriptive activity names to enhance interpretability.

4. Descriptive Variable Names: Variable names were modified for clarity and readability. Special characters were removed, and abbreviations were expanded.

5. Correction of Typo: A typographical error ("BodyBody") in the variable names was corrected.

6. Creating a Tidy Dataset: The final dataset was created by computing the average of each variable for each activity and each subject.

The entire data collection and transformation process was implemented using the "run_analysis.R" R script. For detailed usage instructions and additional background information, refer to the accompanying README.md file.
