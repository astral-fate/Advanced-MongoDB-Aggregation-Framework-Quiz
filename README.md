

### Advanced MongoDB Aggregation Framework Quiz

#### Question 1:
Which of the following code snippets groups the documents in the 'employee' collection by both department number and gender, and then calculates the total salary for each combination of department and gender?

a) `db.employee.aggregate([{$group : {_id :"$dno", gender_id:"$gender",totalSalary: {$sum: "$salary" }}])]`

b) `db.employee.aggregate([{$group : {_id :{dno_id: "$dno", gender_id:"$gender"}, totalSalary: {$sum: "$salary" }}])]`

c) `db.employee.aggregate([{$group : {dno_id: "$dno", gender_id:"$gender",totalSalary: {$sum: "$salary" }}])]`

d) None of the above

<details>
<summary>Answer</summary>
b) `db.employee.aggregate([{$group : {_id :{dno_id: "$dno", gender_id:"$gender"}, totalSalary: {$sum: "$salary" }}])]`
</details>

---

#### Question 2:
Which code snippet below groups the documents in the "employee" collection by department number, computes the average salary for each department, and arranges the results in descending order based on department number?

a) `db.employee.aggregate([{$group:{_id:{$sort:{"_id":-1},averageSalary:{$avg:"$salary"}}}}])`

b) `db.employee.aggregate([{$sort:{"$dno":-1}, {$group:{_id:"$dno",averageSalary:{$avg:"$salary"}}}}])`

c) `db.employee.aggregate([{$group:{_id:"$dno",averageSalary:{$avg:"$salary"}}},{$sort:{"_id":-1}}])`

d) None of the above

<details>
<summary>Answer</summary>
c) `db.employee.aggregate([{$group:{_id:"$dno",averageSalary:{$avg:"$salary"}}},{$sort:{"_id":-1}}])`
</details>

---

#### Question 3:
Which of the following is a valid MongoDB statement?

a) `db.employee.find({'dno': 8}, { 'lname':1,'salary':1}).sort({'salary':asc})`

b) `db.employee.find({ $and:{{'dno': 8}},{'gender': 'm'}} },{' id':0, 'dno':1}).limit(30)`

c) `db.employee.find({ _id':{$ltc:14}},{ _id':0, 'ssn':1}).limit(4).sort({'salary':desc})`

d) None of the above

<details>
<summary>Answer</summary>
d) None of the above
</details>

---

#### Question 4:
Which of the following code groups the documents in the employee collection by department number and calculates the maximum salary of each department?

a) `db.employee.aggregate([ {$group : { _id : null, maxSalary: { $max: "$salary" } } ]])`

b) `db.employee.aggregate([ {$group : { _id : "$dno", maxSalary: { $max: "$salary" } } ]})`

c) `db.employee.aggregate([ {$group : { {$match: {"dno":7} }, maxSalary: { $max: "$salary" } } ]})`

d) None of the above

<details>
<summary>Answer</summary>
b) `db.employee.aggregate([ {$group : { _id : "$dno", maxSalary: { $max: "$salary" } } ]})`
</details>

---

#### Question 5:
Which of the following is not a valid MongoDB statement?

a) `db.sales.insertMany([{'id':11,'item':'abc','price':10,'quantity':2,'date':new Date(2014-03-01T08:00:00Z))]);`

b) `db.people.insertOne({'id':2,'ssn':12,'name':'Mohamed','age':'20')`

c) `db.sales.insertMany([{'id':19},{'item':'jkl}],[{price':5},{'quantity':20})];`

d) None of the above

<details>
<summary>Answer</summary>
c) `db.sales.insertMany([{'id':19},{'item':'jkl}],[{price':5},{'quantity':20})];`
</details>

---

#### Question 6:
Which of the following is not a valid MongoDB statement?

a) `db.project.deleteOne{join_date:$exists:false}`

b) `db.sales.deleteMany{unique:true}`

c) `db.project.deleteMany{id':$not:13}`

d) None of the above

<details>
<summary>Answer</summary>
a) `db.project.deleteOne{join_date:$exists:false}`
</details>

---

#### Question 7:
Which of the following is not a valid MongoDB statement?

a) `db.project.createIndex{ pnumber: 1, Pname: -1 } , { name: 'pno_name' }`

b) `db.project.getAllIndexes()`

c) `db.department.dropIndex('dnumber_1');`

d) None of the above

<details>
<summary>Answer</summary>
a) `db.project.createIndex{ pnumber: 1, Pname: -1 } , { name: 'pno_name' }`
</details>

---

#### Question 8:
Which of the following code calculates the average salary of employees in department 10?

a) `db.employee.aggregate([{$group:{_id:null, averageSalary: { $avg: "Salary"}}}},{$match:{"dno":10} }])`

b) `db.employee.aggregate([{$group:{_id:{"dno":7}, averageSalary: { $avg: "Salary"}}}])`

c) `db.employee.aggregate([{$match:{"dno":10} },{$group:{_id:null, averageSalary: { $avg: "Salary"}}}])`

d) None of the above

<details>
<summary>Answer</summary>
c) `db.employee.aggregate([{$match:{"dno":10} },{$group:{_id:null, averageSalary: { $avg: "Salary"}}}])`
</details>

---

#### Question 9:
Which of the following is not a valid MongoDB statement?

a) `db.sales.updateMany ( {$or: [{_id':{$gte:14, $lte:16}},{price:7.5}]}, { $set : {join_date : "} } )`

b) `db.sales.updateMany ( { '_id':{$gte:14, $lte:16} }, { $unset : {join_date : new Date()} }`

c) `db.sales.updateMany ( { 'join_date':{$exists:True}}, {$set : {start_date: new Date()}}`

d) None of the above

<details>
<summary>Answer</summary>
b) `db.sales.updateMany ( { '_id':{$gte:14, $lte:16} }, { $unset : {join_date : new Date()} }`
</details>

---

#### Question 10:
Which of the following is a valid MongoDB statement?

a) `db.employee.insertOne([ 'ssn': '1234', 'fname': 'AH','dno':'20']);`

b) `db.employee.insertOne({ ssn: 1234,fname: AH, dno: 20});`

c) `db.employee.insertMany({'ssn': '1234', 'fname': 'AH','dno': 10});`

d) None of the above

<details>
<summary>Answer</summary>
d) None of the above
</details>
