# ForExam
# CS
 public Something()
 {
     MySqlConnectionStringBuilder builder = new MySqlConnectionStringBuilder();
     builder.Server = "localhost";
     builder.Database = "DBName";
     builder.UserID = "root";
     this.conn = new MySqlConnection(builder.ToString());
     this.cars = new List<Car>();
     FillCars();

 }
 public void Fill()
 {
     conn.Open();
     MySqlCommand cmd = new MySqlCommand("SELECT * FROM cars", conn);
     MySqlDataReader reader = cmd.ExecuteReader();
     while (reader.Read())
     {
         int id = reader.GetInt32("id");
         Car car = new something(id);
         cars.Add(car);
     }
     conn.Close();           
 }

 # Frontend
