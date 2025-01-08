

1.
   - Question: Which of the following is a valid MongoDB statement?
   - Options:
     - a) `db.employee.find({'dno': 8}, {'Iname':1,'salary':1}).sort{'salary':asc}}`

     - b) `db.employee.find({ $and:['dno': 8},{'gender':'m'] },{_id':0, 'dno':1}.limit(30)`

     - c) `db.employee.find({'_id':{$lte:14}},{'_id':0,'ssn':1}.limit(4).sort{'salary':desc})`
     - d) None of the above
   - Correct Answer: d) None of the above

2. 
   - Question: Which of the following is not a valid MongoDB statement?
   - Options:

     - a) `db.sales.updateMany ({'_id':{$lte:14}}, {$set':{start_date': new Date ()}}}`

     - b) `db.sales.updateMany ({},{$unset:{start_date:''}})`

     - c) `db.sales.updateMany ({'_id':13}, {$unset : {join_date : new Date ()}})`

     - d) None of the above
   - Correct Answer: d) None of the above

3. 
   - Question: Which of the provided code snippets performs a grouping operation on the "employee" collection by department number, calculates the count of employees in each department, and filters the results to retain only departments with more than 4 employees?

   - Options:
     - a) `db.employee.aggregate([$group: {_id:"$dno",count:[$sum:1]}){$,$match:[sum: {sgt:4} }])`
   

  - b) `db.employee.aggregate([$match:[count:[$gt:4]}]{$,$group: {_id:"$dno",count: {ssum:1}]})`


     - c) `db.employee.aggregate([{$group: {_id:"$Sdno",count:{$sum:1}}},{$match:{count: {$gt:4} }} ])`

     - d) None of the above

   - Correct Answer: c) ``db.employee.aggregate([{$group: {_id:"$Sdno",count:{$sum:1}}},{$match:{count: {$gt:4} }} ])`


4. **IMG-20250108-WA0006.jpg**
   - Question: Which of the following code calculates the average salary of employees in department 10?

   - Options:
     - a) `db.employee.aggregate([$group:{id:null, averageSalary:{$avg: "Salary"}}}, {$match: {'dno":10;} }])`

     - b) `db.employee.aggregate([$group:{id:'dno":7), averageSalary:{$avg: "Salary"} }} ])`

     - c) `db.employee.aggregate([$match: {'dno":10} }, {$group:{'_id':null, averageSalary:{ $avg:"$salary"}}} ]);`

     - d) None of the above
   - Correct Answer: c) 

`db.employee.aggregate([$match: {'dno":10} }, {$group:{'_id':null, averageSalary:{ $avg:"$salary"}}} ]);`

5. **IMG-20250108-WA0007.jpg**
   - Question: Which of the following is a valid MongoDB statement?
   - Options:
     - a) `db.employee.createIndex({'ssn':1, name:'ssn1')`
     - b) `db.department.createIndex({'dnumber':1, unique:true}`
     - c) `db.project.createIndex({ pnumber: 1, Pname:0 })`
     - d) None of the above

   - Correct Answer: b) `db.department.createIndex{'dnumber':1,unique:true}`

6. **IMG-20250108-WA0008.jpg**
   - Question: Among the provided code snippets, which one groups the documents in the employee collection by department number and calculates the count of employees in each department?
   - Options:
     - a) `db.employee.aggregate([{$group: { '_id': "$dno", emp:{$count : emp} }}}])`

     - b) `db.employee.aggregate([{$group: { _id: "$dno", emp: {$sum:1} }} ])`
     - c) `db.employee.aggregate([{$group: { _id: "$dno", emp:{ {$sum:emp} } }])`
     - d) None of the above

   - Correct Answer: b) `db.employee.aggregate([{$group: { _id: "$dno", emp: {$sum:1} }} ])`



7. **IMG-20250108-WA0009.jpg**
   - Question: Which of the following is not a valid MongoDB statement?
   - Options:
     - a) `db.sales.insertMany([{'_id':11,'item':'abc','price':10,'quantity':2,'date':new Date(2014-03-01T08:00:002) }]);`

     - b) `db.people.insertOne({'_id':2,'ssn':12,'name':'Mohamed','age':'20')`

     - c) `db.sales.insertMany([{ '_id':19),{'item'':'jk1'}], [{price':5},{'quantity':20}];`
     - d) None of the above
   - Correct Answer: c) `db.sales.insertMany([{ '_id':19),{'item'':'jk1'}], [{price':5},{'quantity':20}];`


8. **IMG-20250108-WA0010.jpg**
   - Question: Which of the following is a valid MongoDB statement?
   - Options:
     - a) `db.employee.insertOne(['ssn': '1234', 'fname': 'AH','dno':'20');`
     - b) `db.employee.insertOne({ssn: 1234, fname: AH, dno: 20});`
     - c) `db.employee.insertMany({'ssn': '1234', 'fname': 'AH','dno': 10});`
     - d) None of the above
   - Correct Answer: d) None of the above


9. **IMG-20250108-WA0011.jpg**
   - Question: Among the given code snippets, which one executes an aggregation operation that joins the 'employee' collection with the 'department' collection based on the 'dno' field?
   - Options:
     - a) `db.employee.aggregate[{$join:{from:"department",localField:"dno",foreignField: "dnumber",as:"employee_dept"}} ])`

     - b) `db.employee.aggregate[{$lookup: from:"department",localField:"dno",foreignField: "dnumber", as:"employee_dept"}} ])`

     - c) `db.department.aggregate([{$lookup: { from:"department:dnumber", as:"employee_dept`}} ])

     - d) None of the above

   - Correct Answer: b) 
`db.employee.aggregate[{$lookup: from:"department",localField:"dno",foreignField: "dnumber", as:"employee_dept"}} ])`

10. **IMG-20250108-WA0012.jpg**

    - Question: Which of the following code snippets groups the documents in the 'employee' collection by both department number and gender, and then calculates the total salary for each combination of department and gender?
    - Options:

      - a) `db.employee.aggregate([$group:{id:"$dno",gender id:"$gender"totalSalary: {$sum:"$salary"}]]}`

      - b) `db.employee.aggregate([{ $group: {_id: { dno_id:"$dno",gender_id:"$gender"}, totalSalary: {$sum:"$salary"}}} ])`

      - c) `db.employee.aggregate([{$group:{dno_id:"$dno",gender_id:"$gender", totalSalary: {$sum:"$salary"}}} ])`

      - d) None of the above

    - Correct Answer: b) `db.employee.aggregate([$group:{id:[dno id:"$dno",gender id:"$gender"), totalSalary: {$sum:"$salary"}]]}`


11. **IMG-20250108-WA0013.jpg**
    - Question: Which of the following is not a valid MongoDB statement?
    - Options:
      - a) `db.sales.updateMany ( {$or: [{id':{$gtc:14, Sltc:16},{price:7.5}], {$set : {join_date :"} }`

      - b) `db.sales.updateMany {{id':{Sgtc:14, Sltc:16}, { $unset : {join_date : new Date()} } }`

      - c) `db.sales.updateMany {{join_date':{$exists:True}, {$set : {start_date: new Date()}}}`

      - d) None of the above
    - Correct Answer: d) None of the above

12. **IMG-20250108-WA0014.jpg**
    - Question: Among the given code snippets, which one executes an aggregation operation that joins the 'department' collection with the 'dept_locations' collection based on the 'dnumber' field?
    - Options:
      - a) `db.department.aggregate( [ { $lookup: { from: "dept_locations", localField: "dnumber", foreignField: "dnumber", as: "dept_location" } } ] )`
      - b) `db.dept_locations.aggregate( [ { $lookup: { from: "department", localField: "dnumber", foreignField: "dnumber", as: "dept_location" } } ] )`
      - c) `db.department.aggregate( [ { $lookup: { from: "dept_locations", on: "dnumber", as: "dept_location" } } ] )`
      - d) None of the above
    - Correct Answer: a) `db.department.aggregate( [ { $lookup: { from: "dept_locations", localField: "dnumber", foreignField: "dnumber", as: "dept_location" } } ] )`

13. **IMG-20250108-WA0015.jpg**
    - Question: Which of the following is not a valid MongoDB statement?
    - Options:
      - a) `db.project.createIndex{ pnumber: 1, Pname:-1 } , { name:'pno_name' }`
      - b) `db.project.getAllIndexes()`
      - c) `db.department.dropIndex('dnumber_1');`
      - d) None of the above
    - Correct Answer: b) `db.project.getAllIndexes()`

14. 
    - Question: Which of the following is not a valid MongoDB statement?
    - Options:
      - a) `db.employee.find{('dno': {$ne:8}}, { 'fname':1,'lname':1,'salary':0}).sort({'salary':-1})`

      - b) `db.employee.find({'dno':{$lte:8} }, {'_id':0,'lname':1,'salary':1}).sort('salary':0})`

      - c) `db.employee.find('dno': 8}, { 'fname':1,'lname':1,'dno':1}).sort('salary':1})`

      - d) None of the above
    - Correct Answer: b) `db.employee.find({'dno':{$lte:8} }, {'_id':0,'lname':1,'salary':1}).sort('salary':0})`



15. **IMG-20250108-WA0017.jpg**
    - Question: Among the given code snippets, which one executes an aggregation operation that joins the 'department' collection with the 'dept_locations' collection based on the 'dnumber' field?
    - Options:
      - a) `db.department.aggregate( [ { $lookup: { from: "employee", localField: "mgrssn", foreignField: "ssn", as: "manager" } } ] )`


      - b) `db.department.aggregate( [ { $lookup: { from: "employee", localField: "mgrssn=ssn", as: "dept_m" } } ] )`


      - c) `db.employee.aggregate( [ { $lookup: { from: "department", localField: "mgrssn", foreignField: "ssn", as: "m" } } ] )`
      - d) None of the above
    - Correct Answer: d) None of the above



16. **IMG-20250108-WA0018.jpg**
    - Question: Which of the following is not a valid MongoDB statement?
    - Options:
      - a) `db.employee.find({'dno':8}, {'fname':1,'Iname':1,'dno':1,'salary':1')}.sort({'salary':1})`

      - b) `db.employee.find('dno>8),['fname':1,'Iname':1,'dno':1,'salary':1').sort (i'salary':1))`

      - c) `db.employee.aggregate([ { $group: { _id: "$dno", averageSalary: { $avg: "$Salary" } } }, { $sort: { _id: -1 } } ])`

      - d) None of the above

    - Correct Answer: b) `db.employee.find('dno>8),['fname':1,'Iname':1,'dno':1,'salary':1').sort (i'salary':1))`



17. **IMG-20250108-WA0019.jpg**
    - Question: Which code snippet below groups the documents in the "employee" collection by department number, computes the average salary for each department, and arranges the results in descending order based on department number?
    - Options:
      - a) `db.employee.aggregate([ { $group:{_id:{ $sort:{"_id":-1), averageSalary:{$avg:"$Salary"}}}} ])`

      - b) `db.employee.aggregate([$sort:{"$dno":-1), {$group:{_id:"$dno",averageSalary:{$avg:"SSalary")}}}}]`
    
  - c) `db.employee.aggregate([ { $group: { _id: "$dno", averageSalary: { $avg: "$Salary" } } }, { $sort: { '_id': -1 } } ])`

      - d) None of the above
    - Correct Answer: c) `db.employee.aggregate([ { $group: { _id: "$dno", averageSalary: { $avg: "$Salary" } } }, { $sort: { _id: -1 } } ])`


18. **IMG-20250108-WA0020.jpg**
    - Question: Which of the given code snippets groups the "employee" collection by department number, computes the employee count for each department, filters the results to include only departments with 5 or fewer employees, and then sorts the documents in descending order based on the employee count?
    - Options:
      - a) `db.employee.aggregate([ { $group:{_id:"$dno",count:{$sum:-1});{$match:[count:${ltc:5} }},{$sort:{"count":-1}}])`

      - b) `db.employee.aggregate([$match:[count: { $lte:5} }},{$sort:{"count":-1}}, {$group: {_id:"$dno",count:{$sum:1}}]`

      - c) `db.employee.aggregate([ { $group:{_id:"$dno",count:{$sum:1} }},{$match:[count:${lte:5} }},{$sort:{"count":-1}}])`

      - d) None of the above

    - Correct Answer: c) `db.employee.aggregate([ { $group:{_id:"$dno",count:{$sum:1} }},{$match:[count:${lte:5} }},{$sort:{"count":-1}}])`


19. **IMG-20250108-WA0021.jpg**
    - Question: Which of the following code groups the documents in the employee collection by department number and calculates the maximum salary of each department?
    - Options:

      - a) `db.employee.aggregate([{ $group : { _id : null, maxSalary: {$max: "$salary"} } }])`

      - b) `db.employee.aggregate([{$group : { -id : "$dno", maxSalary: {$max: "$salary"} } }])`

      - c) `db.employee.aggregate([{$group : { {$match: {"dno":7} }, maxSalary: {$max: "$salary"} } ])`

      - d) None of the above

    - Correct Answer: b) `db.employee.aggregate([{$group : { -id : "$dno", maxSalary: {$max: "$salary"} } }])`
`



20. **IMG-20250108-WA0022.jpg**
    - Question: Which of the following is not a valid MongoDB statement?
    - Options:
      - a) `db.project.deleteOne{'join_date':{$exists:false}})`
      - b) `db.sales.deleteMany({unique': true})`
      - c) `db.project.deleteMany({'_id':{$not:13}} )`
      - d) None of the above
    - Correct Answer: b) `db.sales.deleteMany{unique': true}}`

