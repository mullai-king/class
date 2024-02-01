# THIS IS BIKE COMMAND LINE APPLICATION 

## Consepts used
  - Class
  - Object
  - Spread oprator and basic conditions
## Methods inside class
```
  - getDetails()
  - startBike()
  - stopBike()
  - gearUp()
  - gearDown()
```
### code
```
class Bike{
  constructor(brand,model,engineType,year,maxgear,fuelType){
    this.brand =brand;
    this.model =model
    this.engine = engineType;
    this.year = year;
    this.maxgear = maxgear;
    this.fuelType = fuelType;
    this.gearState =0;
    this.engineStarted = false;
    this.allDetails = [brand,engineType,year,maxgear,fuelType]
  }
  getdetails(){
    console.log(...this.allDetails)
  }
  startBike(){
    if(this.engineStarted ==false){
      console.log("Engine is starting...")
      this.engineStarted =true;
      console.log("Engine Started")
    }
    else{
      console.log("Engine already started!")
    }
  }
  stopBike(){
    if(this.engineStarted==true){
      this.engineStarted=false;
      console.log("Engine stopped")
    }
    else{
      console.log("Engine not yet started")
    }
  }

  gearUp(){
    if(this.gearState>=0 && this.gearState < this.maxgear){
      this.gearState++;
      console.log(`Gear shifted next .Now You're in ${this.gearState} gear`)
    }
    else{
      console.log(`Youre try to shift ${this.gearState+1} gear. But ${this.model} has ${this.gearState} gears`)
    }
  }
  gearDown(){
    if(this.gearState>0 && this.gearState <=this.maxgear){
      this.gearState--;
      console.log(`Gear shifted before.Now You're in ${this.gearState} gear`);
    }
    else{
      console.log("Gear state is Neutral")
    }
  }

}


const dreamNeo = new Bike("Honda","Dream Neo 110","BS IV",2013,4,"petrol");
dreamNeo.getdetails();
dreamNeo.startBike();
dreamNeo.startBike();
dreamNeo.stopBike();
dreamNeo.stopBike();
dreamNeo.startBike();
dreamNeo.gearUp();
dreamNeo.gearUp();
dreamNeo.gearUp();
dreamNeo.gearUp();
dreamNeo.gearUp();
dreamNeo.gearDown();
dreamNeo.gearDown();
dreamNeo.gearDown();
dreamNeo.gearDown();
dreamNeo.gearDown();
dreamNeo.gearDown();
```
### Output
```
Honda BS IV 2013 4 petrol
Engine is starting...
Engine Started
Engine already started!
Engine stopped
Engine not yet started
Engine is starting...
Engine Started
Gear shifted next .Now You're in 2 gear
Gear shifted next .Now You're in 4 gear
Gear shifted before.Now You're in 3 gear
Gear shifted before.Now You're in 2 gear
Gear shifted before.Now You're in 1 gear
Gear shifted before.Now You're in 0 gear
Gear state is Neutral
Gear state is Neutral
```