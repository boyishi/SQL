<b> Database Description </b>
- The company is organized into branches. Each branch has an id, a name
- Each branch must be managed by one of the employees that work there
- Each client has a name and unique id to identify it 
- Each employee has a name, birthday, sex, salary, and a unique number
- An employee can act as a supervisor for other employees at the branch or at other branches. An employee can have at most one supervisor. 
- An employee can work at one branch at a time
- A client has a name and a unique id 
- A client may only be handled by one branch at a time
- Employees can work with clients by their branch. We want to keep track of total sales by each employee
- Many branches will work with suppliers to buy inventory
- Each supplier has a name and the product they're selling
- A supplier may supply products to multiple branches 
  
 <b> Database Design </b>
 ![image](https://user-images.githubusercontent.com/73207981/102832755-edef7680-43b4-11eb-9d02-5bd735419b1d.png)

<b> Database Creation </b>
1. Mapping of Regular Entity Types
2. Mapping of Weak Entity Types 
    * Primary Key should contain the primary key of its owner and its own key
    * ex. Branch Supplier can not exist without a Branch => Branch's primary KEY + it's own primary KEY
3. Mapping of Binary 1:1 relationship types
    * Include one side of the relationship as foreign key in the other 
    * Favor total participation
    * ex. Each branch must have one manager so branch would have mgr_id as a FOREIGN KEY
4. Mapping of Binary 1:N relationship types
    * The N side should have the other's PRIMARY KEY as a FOREIGN KEY
    *  ex. A branch can have many clients but a client must have a branch => client will have branch as a FOREIGN KEY
5. Mapping of Binary M:N relationship types
    * Create a new relation table who's primary key is a combination of both entities' primary keys (BOTH FOREIGN KEYS)
    * Also include any relationship attribute
 
<b> Roadmap </b>

![image](https://user-images.githubusercontent.com/73207981/102854044-39bb1380-43e7-11eb-9173-5b4ddde028ad.png)

<b> Result </b>

![image](https://user-images.githubusercontent.com/73207981/102835794-517da200-43bd-11eb-83ea-a4e8f9a82c13.png)

