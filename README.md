# code45
package dm;
import java.util.Random;
import java.util.Scanner;
public class dm
    {
    public static void main(String[] args) {
        System.out.println("-----随机点名器");
        String[] students=new String[3];
        addStudentName(students);
        printStudentName(students);
        String randomName=randomStudentName(students);
        System.out.println("被点名到的同学是:"+randomName);
    }
    //存储
    public static void addStudentName(String[] students){
        Scanner sc=new Scanner(System.in);
        for(int i=0;i<students.length;i++){
            System.out.println("存储第"+(i+1)+"个姓名:");
            //接收控制台录入的姓名字符串
            students[i]=sc.next();
        }
    }
    //总览
    public static void printStudentName(String[] students){
        System.out.println("总览全班姓名");
        for(int i=0;i< students.length;i++){
            String name=students[i];
            System.out.println(name);
        }
    }
    //随机点名
    public static String randomStudentName(String[] students) {
        int index=new Random().nextInt(students.length);
        String name=students[index];
        return name;
    }

}
