#include<stdio.h>
#include<conio.h>
#include<string.h>
int main()
{
	struct student
	{
		int roll_no;
		char name[80];
		float fees;
		char dob[80];
	};
	
	struct student stud1[50];
	int n,i,rollno,new_rollno;
	float new_fees;
	char new_name[80],new_dob[80];
	
	printf("\nEnter the no of students:\t");  
	scanf("%d",&n);
	
	for(i=0;i<n;i++)
	{
		printf("Student %d:\n\n",i); 
		
		printf("\nEnter the roll no.:\t");  
		scanf("%d",&stud1[i].roll_no);
	
		printf("Enter the name:\t");  
		fgets(stud1[i].name,80,stdin);
	
		printf("\nEnter the fees:\t");  
		scanf("%f",&stud1[i].fees);
	
		printf("\nEnter the date of birth:\t");  
		fgets(stud1[i].dob,80,stdin);
		printf("\n\n");  
	}
	
	printf("\n\nDetails:\n");
	
	for(i=0;i<n;i++)
	{
		printf("Student %d:\n",i); 	
		printf("\nRoll No.       :\t%d",stud1[i].roll_no);
		printf("\nName           :\t%s",stud1[i].name);
		printf("\nFees           :\t%.2f",stud1[i].fees);
		printf("\nDate of Birth  :\t%s",stud1[i].dob);
		printf("\n\n"); 
	}
	
	printf("\nEnter the name of the student whose details you wanna change:\t"); 
	scanf("%d",&rollno);	
	
	printf("Enter the new roll no.:\t");  
	scanf("%d",&new_rollno);
	
	printf("Enter the new name:\t");  
	scanf("%s",new_name);
	
	printf("Enter the new fees:\t");  
	scanf("%f",&new_fees);
	
	printf("Enter the new date of birth:\t");  
	scanf("%s",new_dob);
	
	stud1[rollno].roll_no=new_rollno;
	strcpy(stud1[rollno].name,new_name);
	stud1[rollno].fees=new_fees;
	strcpy(stud1[rollno].dob,new_dob);
	
	for(i=1;i<=n;i++)
	{
		printf("Student %d:\n",i); 	
		printf("\nRoll No.     :\t%d",stud1[i].roll_no);
		printf("\nName         :\t%s",stud1[i].name);
		printf("\nFees         :\t%.2f",stud1[i].fees);
		printf("\nDate of Birth:\t%s",stud1[i].dob);
		printf("\n\n"); 
	}
	return 0;
	
}
