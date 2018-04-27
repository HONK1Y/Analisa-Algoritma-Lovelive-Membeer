class LoveLiveTumpukan {
static int atas = -1;
static int batasAtas = 7;
     public static void push(String tumpukan[], String data)
{
         if(atas >= batasAtas)
         System.out.println("Tumpukan penuh");
         else
{

         System.out.println("PUSH : " + data);
               atas = atas + 1;
               tumpukan[atas] = data;
   }
}
public static String pop(String tumpukan[]){
 String hasilPop = " ";
         if(atas < 0)
         hasilPop = "Tumpukan kosong";
         else
{
hasilPop = tumpukan[atas];
tumpukan[atas] = null;
atas--;
}
return (hasilPop);
}
public static void bacaTumpukan(String tumpukan[]){
         System.out.println("Kondisi tumpukan : ");
            for (int i = batasAtas; i >= 0; i--)
{
            if(i == atas)
         System.out.println(i + "." + tumpukan[i] + "atas");
		 else
         System.out.println(i + "." + tumpukan[i]);

}
}
public static void clearTumpukan(String tumpukan[])
{ 
for (int i= batasAtas; i>=0; i--)
    {
pop(tumpukan);
  
}
    }
public static void main(String args[])
{
String tumpukan[] = new String[10];

push(tumpukan, "Kousaka Honoka");
push(tumpukan, "Sonoda Umi");
push(tumpukan, "Minami Kotori");
System.out.println();
bacaTumpukan(tumpukan);

System.out.println();
push(tumpukan, "Nishkino Maki");
push(tumpukan, "Hoshizora Rin");
push(tumpukan, "Koizumi Hanayo");
System.out.println(); 
bacaTumpukan(tumpukan);

System.out.println();
push(tumpukan, "Yazawa Nico");
push(tumpukan, "Ayase Eli");
push(tumpukan, "Toujo Nozomi");
push(tumpukan, "Takami Chika");
push(tumpukan, "Tsushima Yoshiko");
System.out.println();
bacaTumpukan(tumpukan);

System.out.println();
System.out.println("POP : " + pop(tumpukan)); 
System.out.println("POP : " + pop(tumpukan));   
bacaTumpukan(tumpukan);

System.out.println();
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));
bacaTumpukan(tumpukan);

System.out.println();
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));
System.out.println("POP : " + pop(tumpukan));

clearTumpukan(tumpukan);
bacaTumpukan(tumpukan);
}
}
   
