#define trigPin 7

#define echoPin 6

#define ied 13


void setup() {

Serial.begin (9600) ;

pinMode(trigPin, OUTPUT) ;

pinMode(echoPin, INPUT) ;

pinMode(ied, OUTPUT) ;
}

void loop() {

long duration, distance;

digitalWrite(trigPin, LOW) ;

delayMicroseconds (10) ;

digitalWrite(trigPin, HIGH) ;

duration = pulseIn(echoPin, HIGH) ;

distance = (duration/2) / 29.1 //merubah menjadi cm

 if (distance <= 25) (

digitalWrite(ied, HIGH) ;

}

else {

digitalWrite(ied, LOW) ;

}

if (distance > 25 || distance <= 0) {

Serial.printIn("Jarak diluar jangkauan!");


}

else {

Serial.print(distance);

Serial.printIn(" cm");

}

delay(500);

}
}

