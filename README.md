import java.io.File;
import java.io.IOException;
import java.io.PrintStream;
import java.util.Calendar;
import java.util.Date;
import java.util.Scanner;


public class QuickResume {


	PrintStream fileStream =null;
	Scanner in =new Scanner(System.in);
	Date d=new Date();
	int year = Calendar.getInstance().get(Calendar.YEAR);
	boolean status=true;
	String Name=null;		String mob_no=null;	    String mail_Id=null;
	String addrLine2=null;	String proj=null;		String proj_title=null;
	String Obj=null;		String education=null; 		
	String resume=null;     String Choice;			String tools=null;
	String addrLine1=null;	String city=null;		String state=null;
	String country=null;	String cert1=null;
	String altrMail=null;	String cert2=null;		String proj1=null;		
	String proj_title1=null;String tools1=null;		String cert3=null;
	String edu1=null; 		double edu1_per=0;   	String edu1_ins=null; 
	int edu1_year=0; 		String edu2_ins=null; 	int edu2_year=0;
	String edu2=null; 		double edu3_per=0;		String edu3_ins=null;
	int edu3_year=0;	 	String edu3=null;   	double edu2_per=0;
	String job1=null; 		String job1_tot=null;	String job1_comp=null;

	public QuickResume() {
		
		// TODO Auto-generated constructor stub
	}
	public void getDetails() throws IOException
	{
		//Scanner in =new Scanner(System.in);
		System.out.println("Enter the Name");
		Name=in.nextLine();
		do{
			System.out.println("Enter the Mobile no");
			mob_no=in.nextLine();
			status=false;
			if(mob_no.length()>10 || mob_no.length()<10){
				status=true;
				System.out.println("Entered mobile no has less or more than 10 digits");
			}
		}while(status);
		
		
		System.out.println("Enter the MailId no");
		mail_Id=in.nextLine();
		System.out.println("Enter the Alternate MailID no");
		altrMail=in.nextLine();
		System.out.println("You are entering into Project section");
		System.out.println("Enter the total no of projects needed to enter");
		System.out.println("You will be prompted for");
		System.out.println("1)Title");
		System.out.println("2)Description");
		System.out.println("3) Tools used in the project in the same order");
		System.out.println("In the same order as above for every project");
		System.out.println("PROJECT NO : 1 Enter Title");
			proj_title=in.nextLine();
		System.out.println(" Description");
			proj=in.nextLine();
		System.out.println("Name of the Tools used Type tools");
		System.out.println("ContinuouslySeparated by commas");
			tools=in.nextLine();
		System.out.println("PROJECT NO : 2 Enter Title");
			proj_title1=in.nextLine();
		System.out.println("Description");
			proj1=in.nextLine();
		
		System.out.println("PROJECT NO : 2 Name of the Tools used Type tools");
		System.out.println("Continuously Separated by commas");
			tools1=in.nextLine();
		
		
			System.out.println("Enter the Communication Address");
			
				System.out.println("Enter the Address Line ");
				addrLine1=in.nextLine();
				System.out.println("Enter the Address Line ");
				addrLine2= in.nextLine();
				System.out.print("Enter the City:");
				city=in.nextLine();
				System.out.print("Enter the State:");
				state=in.nextLine();
				System.out.print("Enter the Country");
				country=in.nextLine();
		System.out.println("Enter the Certification Details");
		System.out.println("Certification 1 Name:");
		cert1=in.nextLine();
		System.out.println("Certification 2 Name:");
		cert2=in.nextLine();
		System.out.println("Certification 3 Name");
		cert3=in.nextLine();
		
		System.out.println("Enter your SSC Education Details");
		do{
		System.out.println("Title");
		edu1=in.nextLine();
		}while(edu1!=null);
		
		System.out.println("Institution name");
		edu1_ins=in.nextLine();
		
		do{
			System.out.println("Year of passing");
			edu1_year=in.nextInt();
			status=false;
			if(edu1_year>year){
				status=true;
				System.out.println("Entered year is in future Check your year");
			}
		}while(status);
		do{
			System.out.println(" Percentage no need to enter % symbol <<Format: 98.76>>");
			edu1_per=in.nextDouble();
			status=false;
			if(edu1_per>100){
				status=true;
				System.out.println("Check your entered percentage");
			}
			}while (status);
		
		
		System.out.println("Enter your HSC Education Details");
		System.out.println("Title");
		edu2=in.nextLine();
		
		System.out.println("Institution name");
		edu2_ins=in.nextLine();
		do{
			System.out.println("Year of passing");
			edu2_year=in.nextInt();
			status=false;
			if(edu2_year>year){
				status=true;
				System.out.println("Entered year is in future Check your year");
			}
			}while (status);
		
		do{
			System.out.println("Percentage no need to enter % symbol <<Format: 98.76>>");
			edu2_per=in.nextDouble();
			status=false;
			if(edu2_per>100){
				status=true;
				System.out.println("Check your entered percentage");
			}
			}while (status);
		
		
		System.out.println("Enter your Highest graduation/Post Graduation Education Details");
		System.out.println("Title");
		edu3=in.nextLine();
		
		System.out.println("Institution name");
		edu3_ins=in.nextLine();
		
		System.out.println("Year of passing");
		do{
			System.out.println("Year of passing");
			edu3_year=in.nextInt();
			status=false;
			if(edu3_year>year){
				status=true;
				System.out.println("Entered year is in future Check your year");
			}
			}while (status);
		do{
			System.out.println("Percentage no need to enter % symbol <<Format: 98.76>>");
			edu3_per=in.nextDouble();
			status=false;
			if(edu3_per>100){
				status=true;
				System.out.println("Check your entered percentage");
			}
			}while (status);		
		
		String choice;
		System.out.println("Are you previously employed? (y/n)");
		choice=in.nextLine();
		if(choice.equalsIgnoreCase("y"))
		{
			System.out.println("Last Job Title");
			job1=in.nextLine();
			System.out.println("Last Company/ Organisation name");
			job1_comp=in.nextLine();
			System.out.println("Total Experience");
			job1_tot=in.nextLine();
		}
		else
		{
			job1		=	"N/A";
			job1_comp	=	"N/A";
			job1_tot	=	"Fresher";
		}
		System.out.println("\nType your Objectives in a single line");
				Obj=in.nextLine();
	/*String resume=Name +"\n EMAIL ID : "+mail_Id + "\n ALT.MAILID :"+altrMail +
					"\n"+addrLine1+"\n"+addrLine2+"\n" + mob_no + "\n\n OBJECTIVE:\n"+Obj+
					"\n\nJOB EXPERIENCE\n"+job1+"\t"+job1_comp+"\t"+job1_tot+
					"\n\nEDUCATIONAL QUALIFICATION\n"+"Qualification\tInstitution\tPercentage\tYear Of Passing\n"
					+edu1+"\t"+edu1_ins+"\t"+edu1_per+"\t"+edu1_year+"\n"+edu2+"\t"+edu2_ins+"\t"+edu2_per+"\t"+edu2_year+
					"\n"+edu3+"\t"+edu3_ins+"\t"+edu3_per+"\t"+edu3_year+
					"\n\n PROJECT DETAILS\n TITLE : "+proj_title+"\nDESCRIPTION\n"+"\t" +proj+
					"\n"+ tools +"\nTITLE : "+proj_title1+"\nDESCRIPTION\n"+"\t" +proj1+"\n"+tools1+
					"\n\nCERTIFICATIONS LIST\n"+"\t"+cert1+"\n\t"+cert2+"\n\t"+cert3;
	System.out.println(resume);*/
				String []resume1={Name ," EMAIL ID : "+mail_Id, "ALT.MAILID :"+altrMail,
						"   "+addrLine1,"   "+addrLine2,"   "+city,"   "+state,"   "+country,
						"   "+mob_no, "OBJECTIVE:","     	"+Obj,
						"JOB EXPERIENCE",job1+"	"+job1_comp+"	"+job1_tot,
						"EDUCATIONAL QUALIFICATION","Qualification		Institution			Percentage	YOP",
						edu1+"	 "+edu1_ins+" 			"+String.valueOf(edu1_per)+"		"+String.valueOf(edu1_year),
						edu2+"	 "+edu2_ins+"			"+String.valueOf(edu2_per)+"		"+String.valueOf(edu2_year),
						edu3+"	 "+edu3_ins+"			"+String.valueOf(edu3_per)+"		"+String.valueOf(edu3_year),
						" PROJECT DETAILS", "TITLE : "+proj_title,"DESCRIPTION", proj,
						"Tools : "+tools," ","TITLE : "+proj_title1,"DESCRIPTION", proj1,"Tools : "+tools1,
						"CERTIFICATIONS LIST","   	"+cert1,"    	"+cert2,"    	"+cert3};
				@SuppressWarnings("resource")
				PrintStream fileStream = new PrintStream(new File("E:\\genResume.txt"));
				for (String resume2: resume1) {
					fileStream.println(resume2);
					fileStream.println(" ");
				}
				System.out.println("Success your resume template is ready in the given location");
				}
	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
	QuickResume rm=new QuickResume();
	rm.getDetails();
	}
	}

	/**
	 * @param args
	 */
