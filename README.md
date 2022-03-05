Java döngüler ile 0'dan girilen sayıya kadar olan sayılardan 3 ve 4'e tam bölünen sayıların ortalamasını hesaplayan programı yazınız.

import java.util.Scanner;

public class Odev17 {


        public static void main(String[] args) {
            //Degiskenleri tanimladim.
            int number,sum=0,count=0,average;

            //Kullanıcıdan veri almak için Scanner sınıfı
            Scanner input = new Scanner(System.in);


            System.out.print("Enter a number : ");
            number = input.nextInt();

            //Kullanıcıdan alınan değere kadar olan sayılardan 3'ün ve 4'ün katı olanları ve kaç tane olduklarını bulun.
            for (int i = 1; i<number; i++){
                if (i % 3 == 0 && i%4 ==0){
                    System.out.println("Number :");
                    System.out.println(i);
                    sum += i;
                    count++;
                }
            }

            //Döngüden sonra sayıların kendi aralarında toplamını, kac adet olduklarını ve ortalama değeri bastırma.
            average = sum / count;
            System.out.println("Average of Numbers Divided by 3 and 4 : " + average);
            System.out.println("Number of values : " + count );

        }
    }
