# c-
עזרה במחלקה ותוכנית ראשית
 class Program
{
    static System.Collections.ArrayList tel_book_arr = new System.Collections.ArrayList();  
    static void Main(string[] args)
    {

        int sel=0;

        while (sel != 6)
        {
            Console.Clear(); 
            Console.WriteLine("1 : enter information");
            Console.WriteLine("2 : display information");
            Console.WriteLine("3 : search information");
            Console.WriteLine("4 : edit information");
            Console.WriteLine("5 : delete information");
            Console.WriteLine("6 : exit");

            Console.WriteLine("enter your choose : ");
            sel = Convert.ToInt32(Console.ReadLine());

            switch (sel)
            {
                case 1:
                    enter_info(); 
                    break;
                case 2:
                    show_info(); 
                    break;
                case 3:
                    search_info();
                    break;
                case 4:
                    edit_info();
                    break;
                case 5:
                    delet_info();
                    break;
            }
        }

    }

    static void enter_info()
    {
        Console.Clear();

        telephone t = new telephone();

        Console.WriteLine("enter name : ");
        t.name = Console.ReadLine();

        Console.WriteLine("enter family : ");
        t.family = Console.ReadLine();

        Console.WriteLine("enter tel : ");
        t.tel = Console.ReadLine();

        tel_book_arr.Add(t); 
    }

    static void show_info()
    {
        Console.Clear();

        foreach (telephone temp in tel_book_arr)
        {
            Console.WriteLine("name : " + temp.name);
            Console.WriteLine("family : " + temp.family);
            Console.WriteLine("tel : " + temp.tel);
            Console.WriteLine(); 
        }
    }

   
    static void edit_info()
    {
        Console.Clear();
        search_info();
    }
    static void delet_info()
    {
        Console.Clear();
    }

    public static object name { get; set; }

    public static object family { get; set; }
}
    public static void search_info()
    {
        Console.Clear();
        object name = Console.WriteLine("please enter the number");
        object family = Console.WriteLine("please enter the family");
    }

class telephone
{
    public string name, family, tel;
}

}
