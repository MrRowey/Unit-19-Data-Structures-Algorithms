```c#
namespace DataStructure
{
    internal class Program
    {
        // Person Structure
        struct Player
        {
            private int LocY;
            private int LocZ;
            private int LocX;
            private int Health;
            private int Stamina;
            private int Speed;


            // Functions using the structure
            
            // Get location of the Player
            public void getLocation()
            {
                Console.WriteLine("X: " + LocX + "\nY: " + LocY + "\nZ: " + LocZ);
            }

            // Set XYZ location of the Player

            public int setLocationX()
            {
                Console.Write("X Location: ");
                return LocX = Convert.ToInt32(Console.ReadLine());
            }
            public int setLocationY()
            {
                Console.Write("Y Location: ");
                return LocY = Convert.ToInt32(Console.ReadLine());
            }
            public int setLocationZ()
            {
                Console.Write("Y Location: ");
                return LocZ = Convert.ToInt32(Console.ReadLine());
            }

            // Set the Player Stamina
            public int setStamina()
            {
                Console.Write("Player Stamina: ");
                return Stamina = Convert.ToInt32(Console.ReadLine());
            }

            // Set the Speed of the Player based on thier Staminter
            public int maxSpeed(int s)
            {
                return Speed = s * Stamina / 2;
            }

            public void getPlayerDetials()
            {
                Console.WriteLine("Player Details");
                Console.WriteLine("-------------------");
                Console.WriteLine("Player Location: " + LocX + " " + LocY + " " + LocZ);
                Console.WriteLine("Player Health: " + Health);
                Console.WriteLine("Player Staminer: " + Stamina);
                Console.WriteLine("Player Speed: " + Speed);
            }

        }

        struct Tank
        {
            public int Armor;
            public int Speed;
            public int Damage;
            public int Weight;
            public bool CanFire;
            public int Capacity;


            // Get All the Details of the tank

            public void getTankDetials()
            {
                Console.WriteLine("Tank Details"
                    + "\n------------"
                    + "\nArmor: " + Armor
                    + "\nSpeed: " + Speed
                    + "\nDamage: " + Damage
                    + "\nWeight: " + Weight
                    + "\nCapacity: " + Capacity
                    );
            }

            // Setting all the details of the tank
            public int setTankDetails(int armor, int damage, int weight, int capacity)
            {
                this.Armor = armor;
                this.Damage = damage;
                this.Weight = weight;
                this.Capacity= capacity;

                return 1;
            }

            // Check to see if the tank is able to Shoot if the Capacity is Greather than 1
            public bool canFire()
            {
                if (Capacity >= 1)
                {
                    Console.WriteLine("Can fire");
                    return CanFire = true;
                }
                else
                {
                    Console.WriteLine("Cant Fire");
                    return CanFire = false;
                }
            }

            // Speed is detamins by the Weight of the tank
            public int setMaxSpeed()
            {
                Console.WriteLine("Set Max Speed");
                int max = Convert.ToInt32(Console.ReadLine());
                int w = this.Weight;

                return Speed = max * w / 3 ;
            }

            // Caculates the Damges to the tank armor
            public int dmgToArmor()
            {
                int a = this.Armor;
                int d = this.Damage;

                return Armor = a / d;
            }


        }

        static void Main(string[] args)
        {
            Tank t = new Tank();

            t.getTankDetials();

            t.setTankDetails(100, 10, 20, 6);

            t.dmgToArmor();

            t.getTankDetials();

            Console.ReadKey();
        }
    }
}

```