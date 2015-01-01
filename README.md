Old-MacDonald
=============
public interface Domesticated
{
  public String getSound();    
  public String getType();
}

public class Cow implements Domesticated
{
  private String myType;
  private String mySound;

  public Cow()
  {
    myType = "Cow";
    mySound = "moo";
  }

  public String getSound()
  {
 return mySound; 
  }

  public String getType()
  {
 return myType; 
  }
}

public class NamedCow extends Cow 
{
    private String Cowsname;

    /**
     * Constructor for objects of class NamedCow
     */
    public NamedCow(String name)
    {
        Cowsname = name;
    }
    public String getName()
    {
   return Cowsname;
   }
   public class Pig implements Domesticated

{
  private String myType;
  private String mySound;

  public Pig()
  {
    myType = "Pig";
    mySound = "oink";
  }

  public String getSound()
  {
 return mySound; 
  }

  public String getType()
  {
 return myType; 
  }
}
public class Chick implements Domesticated

{
  private String myType;
  private String mySound;
  private boolean confused = false;
  
  

  public Chick()
  {
  myType = "Chick";
  mySound = "chirp";
  }
  
  public Chick(boolean confused)
  {
      this();
      this.confused = confused;
      
  }
  
 
 
  
  
  public String getSound()
  {
      
      
      
  String cheep = "cheep";
  String cluck = "cluck"; 
  
 Random generator = new Random();
int choice = generator.nextInt(2);

       if ( confused)
      { 
          
             if( choice == 1)
             {
               return "cluck";
             }
        
            else
            {
            return "cheep";
            }
    }
       
    else
        return mySound;
          
      
    
  
  }

  public String getType()
  {
 return myType; 
  }
  
  

}
public class Farm
{
      private Domesticated[] myFarm;
	
	   public Farm() 
	   {
		   myFarm = new Domesticated [5];
   myFarm[0] = new Cow();
   myFarm[1] = new Chick();
   myFarm[2] = new Pig();
   myFarm[3] = new Chick(true);
   myFarm[4] = new NamedCow("Elsie");
	   }
	
	   public void animalSounds()
 	   {
		   Domesticated temp;
		   for(int i = 0; i < myFarm.length; i++)
 			{
			   temp = myFarm[i];
			   System.out.println(temp.getType() + " goes " + temp.getSound());
		   }
		    
		   NamedCow named = (NamedCow)myFarm[4];
		   System.out.println(named.getName());
		}
}
public class Driver
{
   public static void main()
   {
       Farm Something = new Farm();
       Something.animalSounds();
       
      

    }
}
   
The digitization of the familiar childhood scene. 
