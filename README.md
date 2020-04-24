package uts4;

public class TextBook
    {
        private String title;
        private String author;
        private String publisher;
        
        public TextBook(String textTitle, String auth, String pub)
        {
            title = textTitle;
            author = auth;
            publisher = pub;
        }
        
        public TextBook(TextBook object2)
        {
            title = object2.title;
            author = object2.author;
            publisher = object2.publisher;
        }
        
        public void set(String textTitle, String auth, String pub)
        {
            title = textTitle;
            author = auth;
            publisher = pub;
        }
        public String toString()
        {
            String str = "\nTitle :"+title+"\nAuthor : "+author+"\nPublisher : "+publisher;
            return str;
        }
    }

package uts4;

public class Instructor
    {
        private String lastName;
        private String firstName;
        private String officeNumber;

        public Instructor (String lname, String fname, String office)
        {
            lastName = lname;
            firstName = fname;
            officeNumber = office;
        }
        
        public Instructor(Instructor object2)
        {
            lastName = object2.lastName;
            firstName = object2.firstName;
            officeNumber = object2.officeNumber;
        }

        public void set (String lname, String fname, String office)
        {
            lastName = lname;
            firstName = fname;
            officeNumber = office;
        }

        public String toString()
        {
            String str = "\nLast Name : " + lastName + "\nFisrt Name : " + firstName + "\nOffice Number : " + officeNumber;
            return str;
        }
    }

package uts4;

public class Course
    {
        private String courseName;
        private Instructor instructor;
        private TextBook textBook;
        
        public Course(String name, Instructor instr, TextBook text)
        {
            courseName = name;
            instructor = new Instructor(instr);
            textBook = new TextBook(text);
        }
        
        public String getName()
        {
            return courseName;
        }
        
        public Instructor getInstructor()
        {
            return new Instructor(instructor);
        }
        
        public TextBook getTextBook()
        {
            return new TextBook(textBook);
        }
        
        public String toString()
        {
            String str = "Course Name :"+courseName+"\nInstructor Information : "+instructor+"\nTextbook Information :"+textBook;
            return str;
        }
    }

package uts4;

    public class CourseDemo
    {
    public static void main(String[] args)
        {
            Instructor myInstructor = new Instructor("Juwita", "Ajeng", "24FP");
            TextBook myTextBook = new TextBook("LASKAR", "Raja Untuk Ratu", "Gaddis");
            Course myCourse=new Course("Intro to Java", myInstructor, myTextBook);
            System.out.println(myCourse);
        }
    }   
