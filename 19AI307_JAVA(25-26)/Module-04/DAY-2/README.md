# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
A smart city has a grid of sensors installed across various zones to monitor Air Quality (AQI).
There are multiple SmartControllers subscribed to this network. Each SmartController is responsible for a specific AQI range:
GreenZoneController: AQI < 100
AlertZoneController: AQI between 100 and 200
DangerZoneController: AQI > 200
When a sensor reports data, only the relevant controller(s) should be notified based on the AQI.

## AIM:
To implement a smart city sensor system where controllers are notified based on specific AQI ranges using observer pattern.


## ALGORITHM :
1.Create sensor network that maintains list of subscribed controllers
2.Implement three controllers (GreenZone, AlertZone, DangerZone) with specific AQI ranges
3.When sensor data arrives, notify only relevant controllers based on AQI value
4.Controllers display alerts only for their designated ranges





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Observer {
    void update(String sensorId, int aqi);
}

interface Subject {
    void registerObserver(Observer observer);
    void removeObserver(Observer observer);
    void notifyObservers(String sensorId, int aqi);
}

class SensorNetwork implements Subject {
    private List<Observer> observers = new ArrayList<>();
    
    @Override
    public void registerObserver(Observer observer) {
        observers.add(observer);
    }
    
    @Override
    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }
    
    @Override
    public void notifyObservers(String sensorId, int aqi) {
        for (Observer observer : observers) {
            observer.update(sensorId, aqi);
        }
    }
    
    public void receiveData(String sensorId, int aqi) {
        System.out.println("Sensor " + sensorId + " reports AQI: " + aqi);
        notifyObservers(sensorId, aqi);
    }
}

class GreenZoneController implements Observer {
    @Override
    public void update(String sensorId, int aqi) {
        if (aqi < 100) {
            System.out.println("[GreenZoneController]: AQI is good at Sensor " + sensorId + ". No action needed.");
        }
    }
}

class AlertZoneController implements Observer {
    @Override
    public void update(String sensorId, int aqi) {
        if (aqi >= 100 && aqi <= 200) {
            System.out.println("[AlertZoneController]: Moderate AQI at Sensor " + sensorId + ". Send public health alert.");
        }
    }
}

class DangerZoneController implements Observer {
    @Override
    public void update(String sensorId, int aqi) {
        if (aqi > 200) {
            System.out.println("[DangerZoneController]: Critical AQI at Sensor " + sensorId + "! Trigger lockdown protocol.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        SensorNetwork sensorNetwork = new SensorNetwork();
        
        sensorNetwork.registerObserver(new GreenZoneController());
        sensorNetwork.registerObserver(new AlertZoneController());
        sensorNetwork.registerObserver(new DangerZoneController());
        
        int n = scanner.nextInt();
        
        for (int i = 0; i < n; i++) {
            String sensorId = scanner.next();
            int aqi = scanner.nextInt();
            sensorNetwork.receiveData(sensorId, aqi);
        }
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="1265" height="261" alt="image" src="https://github.com/user-attachments/assets/606c5e4f-bcb2-4a9c-b25c-bfc6cbd49da6" />



## RESULT:
The smart city sensor system was successfully implemented. Each controller was correctly notified only when AQI fell within its specific range, demonstrating effective selective notification based on observed data.
