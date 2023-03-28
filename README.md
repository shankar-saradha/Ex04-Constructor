# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1:
 Start the C# program using console.App in visual studio 2022
 ### Step2:
 Create a Class and Constructor 
 ### Step3:
 Get employee name, Designation, No of experience, basic salary and insurance amount from the User.
 ### step4:
 Call salary method in constructor to calculate salary.
 ### Step5:
 Call display method to display the output.
 ### Step6:
 Run the program.
## Program:
```c#
using System;
namespace employee
{
    class employee
    {
        public string name, designation;
        public int no_exp, salary, insurance;
        public double hra, ta, basic_pay;


        public employee(string name, string designation, int no_exp, int salary, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.no_exp = no_exp;
            this.salary = salary;
            this.insurance = insurance;

        }
        public void Salary()
        {
            hra = this.salary * 0.2;
            ta = this.salary * 0.1;
            basic_pay = this.salary + hra + ta - this.insurance;
        }
        public void display()
        {
            Console.WriteLine("Employee name {0} , {1} of experience, working as {2}", this.name, this.no_exp, this.designation);
            Console.WriteLine("monthly {0} of salary", basic_pay);
        }
    }
    class employeeDeatils
    {
        public static void Main(string[] args)
        {
            employee emp1 = new employee("Ashwin", "Tester", 10, 30000, 1000);
            emp1.Salary();
            employee emp2 = new employee("Prathap", "Developer", 5, 25000, 1000);
            emp2.Salary();

            emp1.display();
            emp2.display();
        }
    }

}
```

 ## Output:
 ![Csharp exp](https://user-images.githubusercontent.com/93978702/228172896-4b2b6e8d-599e-4ce2-a7fd-a93378a94861.png)

 ## Result:
Thus C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
