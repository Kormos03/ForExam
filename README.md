# ForExam
# CS
```
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
```
 # Frontend
 ```
 const response = await fetch("http://localhost:3000/api/members", {
                method: "POST",
                headers:{
                    Accept: "application/json",
                    "Content-Type": "application/json"
                },
                body: JSON.stringify(memberToSend)
            })
 ```
 Bootstrap cards algorithm:
 ```
  function ToCards(members: Member[]){
        return <div className="row">
            {
                members.map((member) => {
                    return <div className="col sm-4 md-3 lg-2">
                        <div className="card border-dark">
                            <div className="card-body">
                                <h3>{member.name}</h3>
                                <p>{member.birth_date}</p>
                                <p>{member.created_at}</p>
                                {Picture(member)}
                            </div>
                        </div>
                    </div>
                })
            }
        </div>
    }
```
       
