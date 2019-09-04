

SOLUTIONS:
assi code
QUESTION 1:

package com.fpp;

public class Prog1 {

public static void main(String[] args) {
//1. get a random number x in the range 1 .. 9 and compute πx.
int x=RandomNumbers.getRandomInt(1, 9);
System.out.println("x:" + x);
System.out.println("πx:" + Math.pow(Math.PI, x));

//2. get a random number y in the range 3 .. 14 and compute yπ.
int y= RandomNumbers.getRandomInt(3, 14);
System.out.println("y:"  + y);
System.out.println("yπ:"  + Math.pow(y, Math.PI));
}

}
/*

OUTPUT:
x:7
πx:3020.2932277767914
y:14
yπ:3987.194457670312
*/

QUESTION 2:

public class Prog2 {

public static void main(String[] args) {

float num1= 1.27f;
float num2 = 3.881f;
float num3= 9.6f;

System.out.println("Number1:"  + num1 + " \tNumber2:" + num2 + " \tNumber3:" + num3);
//1. the sum of the floats as an integer, obtained by casting the sum to type int
int sumAInteger = (int) (num1 + num2 + num3);
System.out.println("the sum of the floats as an integer:"  + sumAInteger);
//2. the sum of the floats as an integer, obtained by rounding the sum to the nearest integer, using the Math.round function
int sumAIntegerRounding = Math.round(num1 + num2 + num3);
System.out.println("the sum of the floats as an integer(rounding):"  + sumAIntegerRounding);
int sumAIntegerRounding2 = (int) Math.round(num1 + num2 + num3);
System.out.println("the sum of the floats as an integer(rounding)2:"  + sumAIntegerRounding2);
}
}

OUTPUT:
/
Number1:1.27 Number2:3.881 Number3:9.6
the sum of the floats as an integer:14
the sum of the floats as an integer(rounding):15
the sum of the floats as an integer(rounding)2:15 /

QUESTION 3:

package com.fpp;

public class Prog3 {
public static void main(String[] args){
//column names: productId, name,numInStock,provider,pricePerUnit
String records = "231A,Light Bulb,123,Wilco,1.75:"+
"113D,Hairbrush,19,Aamco,3.75:"+
"521W,Shampoo,24,Acme,6.95:"+
"440Q,Dishwashing Detergent,20,Wilco,1.75:"+
"009G,Toothbrush,77,Wilco,0.85:"+
"336C,Comb,34,Wilco,0.99:"+
"523E,Paper Pad Set,109,Congdon and Chrome,2.45:"+
"888A,Fake Diamond Ring,111,AmericusDiamond,3.95:"+
"176A,Romance Nove1 1,20,Barnes and Noble,3.50:"+
"176B,Romance Nove1 2,20,Barnes and Noble,3.50:"+
"176C,Romance Nove1 3,20,Barnes and Noble,3.50:"+
"500D,Floss,44,Wilco,1.25:"+
"135B,Ant Farm,5,Wilco,8.00:"+
"211Q,Bicycle,9,Schwinn,75.95:"+
"932V,Pen Set,50,Congdon and Chrome,9.95:"+
"678Q,Pencil 50,123,Congdon and Chrome,9.95:"+
"239A,Colored Pencils,25,Congdon and Chrome,4.75:"+
"975B,Shower Curtain,25,Wilco,6.50:"+
"870K,Dog Bowl,15,Wilco,4.75:"+
"231S,Cat Bowl,15,Wilco,4.75:"+
"562M,Kitty Litter,15,Wilco,3.25:"+
"777X,Dog Bone,15,Wilco,4.15:"+
"933W,Cat Toy,15,Wilco,2.35:"+
"215A,Hair Ball,0,Little Jimmy,0.00:";
// Implement the code
System.out.println("productId");
System.out.println("----------");
String[] splitRecord = records.split(":");

 for(String eachRecord : splitRecord)
 {
   System.out.println(eachRecord.split(",")[0]);
 }
}

}
OUTPUT:

/*
231A
113D
521W
440Q
009G
336C
523E
888A
176A
176B
176C
500D
135B
211Q
932V
678Q
239A
975B
870K
231S
562M
777X
933W
215A
*/

QUESTION 4:
import java.util.Scanner;

public class Prog4 {

public static void main(String[] args) {
Scanner in = new Scanner(System.in);
System.out.print("Enter String to Reverse:");
String stringToReverse = in.nextLine();

StringBuilder temp = new StringBuilder();
int len = stringToReverse.length() -1;
for (int i= len; i >= 0; --i)
{
  temp.append(stringToReverse.charAt(i));
}
System.out.println("Reversed String:" + temp.toString());
}

}
OUTPUT:
/
Enter String to Reverse:Hello
Reversed String:olleH /

import java.util.Arrays;
import java.util.Scanner;

public class Prog1 {

public Prog1() {
// TODO Auto-generated constructor stub
}

public static void main(String[] args) {
TODO Auto-generated method stub
ss

public class Prog5 {

public static void main(String[] args) {
int[][] elementarySchoolData = new int[4][4];
int len = elementarySchoolData.length;

for (int i = 0; i < len; ++i) {
  for (int k = 0; k < len; ++k) {
     elementarySchoolData[i][k] = RandomNumbers.getRandomInt(1, 99);
  }
}

    for (int a = 0; a < len; ++a) {

  for (int b = 0; b < len; ++b) {

    if (a % 2 == 1 ) {

       System.out.printf("+ %d \t ", elementarySchoolData[a][b] );

       if(b == len -1)
       {
         int k= 0;
         System.out.println();
         while( k < len)
         {
         //System.out.print("____\t  ____\t ____\t ____");
           System.out.print("____\t ");
           ++k;
         }
         System.out.println();

       }


    } else

      System.out.printf("  %d \t ", elementarySchoolData[a][b]);


  }

  System.out.println();


}
}

}

QUESTION 6:

public class Prog6 {

public static void main(String[] args) {
String[] arrayWithDuplicate = {"horse", "dog", "cat", "horse","dog"};

String[] arrayWithoutDuplicate = new String[5] ;

int k=0;
for(String item :arrayWithDuplicate)
{
  if (!checkForDuplicate(item,arrayWithoutDuplicate))
 {
    arrayWithoutDuplicate[k]= item;
    ++k;
 }


}
for(String arrayItem : arrayWithoutDuplicate)
{
  if (arrayItem != null)System.out.println( arrayItem);
}
}

public static boolean checkForDuplicate(String item, String[] arr)
{
for(String element : arr)
{
if (item.equals(element))
return true;
}

return false;
}

}

System.out.println ("Here i come Raundom Numbers");
Scanner sc = new Scanner(System.in);
System.out.print("Write ");
System.out.println(sc.next());
for(int i = sc.next().length())x
sc.close();
String top = "",down = "", line = "";
for(int i = 0; i < 8; i=+2) { top += String.format("%3d/t/t", 90);
down += String.format("%4d\t\t", 7);
line += "__ \t \t";
}
System.out.println(top+"\n"+down+"\n"+line);

 System.out.println("jjj")

duplicatesRemove();

String a = "k";
a.st
}

static void duplicatesRemove() {
String[] original = {"horse", "dog", "cat", "horse","dog"};
String[] newInput = new String[original.length];
for(int i = 0; i < original.length; i++) {
for(int y = 0; y < newInput.length; y++) {
if(!original[i].equals(newInput[y]))
newInput[y] = original[i];

  }
}

System.out.println(Arrays.toString(newInput));
}
}

QUESTION 7:

public class Prog7 {

public static void main(String[] args) {

if(args == null || args.length <0) 
{
  System.out.println("Invlaid Parametr!");
}
else
{
    int len = args.length;
  int countStartWithA =0;

  for(int i = 0; i < len; ++i) {  
    System.out.println("String Input:" + args[i] +  "  Length:" +  args[i].length());
    countStartWithA = args[i].startsWith("A") ? ++countStartWithA: countStartWithA;
  }

  System.out.println("Number of String Inputs start with ‘A’:" + countStartWithA);
}
}

}# QUESTION-1
JAVA ASSI MUM
