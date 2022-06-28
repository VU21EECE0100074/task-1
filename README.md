# task-1
#create an excel sheet containing marks of 5 subjects for 10 students out of 100,import the file into Pandas Dataframe. Plot the pie chart for marks in each subjecr showing the number of students secured a)More than 90 b)More than 80. Compute the total marks for each student. Calculate the perccentage of individual student.
import pandas as pd
import matplotlib.pyplot as plt
import openpyxl
students_marks=pd.read_excel('marks.xlsx')
print(students_marks[students_marks["English"]>90])
print(students_marks[students_marks["Python"]>90])
print(students_marks[students_marks["VDC"]>90])
print(students_marks[students_marks["Chemistry"]>90])
print(students_marks[students_marks["Physics"]>90])
fig,axes=plt.subplots(nrows=3,ncols=2)
fig.set_figheight(8)
fig.set_figwidth(6)
axes[0,0]=students_marks['English'].value_counts().plot(kind='pie',autopct='%.2f%%',ax=axes[0,0])
axes[0,0].set_title('English Marks')

axes[0,1]=students_marks['Python'].value_counts().plot(kind='pie',autopct='%.2f%%',ax=axes[0,1])
axes[0,1].set_title('Python Marks')

axes[1,1]=students_marks['VDC'].value_counts().plot(kind='pie',autopct='%.2f%%',ax=axes[1,1])
axes[1,1].set_title('VDC')

axes[1,0]=students_marks['Chemistry'].value_counts().plot(kind='pie',autopct='%.2f%%',ax=axes[1,0])
axes[1,0].set_title('Chemistry Marks')

axes[2,0]=students_marks['Physics'].value_counts().plot(kind='pie',autopct='%.2f%%',ax=axes[2,0])
axes[2,0].set_title('Physics Marks')
English= float(input("Please enter English Marks: "))
Python = float(input("Please enter Python score: "))
VDC = float(input("Please enter VDC Marks: "))
physics = float(input("Please enter Physics Marks: "))
python = float(input("Please enter python Marks: "))
 
total = maths + english + BEEE + physics + python
average = total / 5
percentage = (total / 500) * 100
 
print("\nTotal Marks = %.2f"  %total)
print("Average Marks = %.2f"  %average)
print("Marks Percentage = %.2f"  %percentage)
