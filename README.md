# ArrayList-first
Primera de U3
class Lista
    {
        int grupos, alumnos, calificaciones;
        //Creacion de listas
        ArrayList List;
        ArrayList List1;
        public Lista()
        {
            List = new ArrayList();
            List1 = new ArrayList();

        }
        
        public void IngresoDeDatos()
        {
            Console.WriteLine("¿Cuantas clases son?");
            grupos = int.Parse(Console.ReadLine());
           
            for(int r=0;r<grupos;r++)
            {
                Console.WriteLine("¿Cuantos hay en cada grupo: {0}?", r+1);
                alumnos = int.Parse(Console.ReadLine());
                List.Add(alumnos);
            }

            for (int r = 0; r < List.Count; r++)
            {
                Console.WriteLine("Ingresa calificaciones de cada grupo:");
                calificaciones = int.Parse(Console.ReadLine());
                List1.Add(calificaciones);

            }
        }
//Uso de foreach para presentar los datos
        public void Imprime()
        {
            Console.WriteLine("Cantidad de alumnos por grupo:");
            foreach(var pug in List)
            {
                Console.WriteLine(pug);
            }

            Console.WriteLine("Calificacion por grupo:");
            foreach (var pong in List1)
            {
                Console.WriteLine(pong);
            }

            Console.ReadKey();
        }
    }
    /////////////////////////////////////
    static void Main(string[] args)
        {
            Lista Obj = new Lista();
            Obj.IngresoDeDatos();
            Console.Clear();
            Obj.Imprime();
            Console.ReadKey();
        }
