import csv
def read_csv(filename):
student_data =
with open(filename, ') as f:
reader = csv.reader (f)
next(reader)
for row in reader:
student_data.append(row)
return student_data
def calculate_average_grades(student_data):
grades_dict = {}
for row in student_data:
if row[0] not in grades_dict:
grades_dict[row[0]] [float(row [2]]]
else:
grades_dict[row[0]].append(float(row[2]))
return [(key, sum(value) / len(value)) for key, value in grades_dict.it
def write_csv(filename, data):
with open(filename, 'w', newline='') as f:
writer = csv.writer (f)
if __name_
writer.writerow(['Name', 'Average Grade']) 
writer.writerows(data)
ain__':
input_filename 'student_data.csv'
output_filename = 'average_grades.csv
student_data = read_csv(input_filename)
average_grades = calculate_average_grades (student_data)
write_csv(output_filename, average_grades)
student data = read cavs(input_ filename) 
calculate _average'
