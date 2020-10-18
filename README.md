# R3training
this is the code i did for moving the motors clockwise.
void setup()
{
  pinMode(11, OUTPUT); //enable 3&4
  pinMode(10, OUTPUT); //enable 1&2
  pinMode(7, OUTPUT); //input 4
  pinMode(6, OUTPUT); //input 3
  pinMode(5, OUTPUT); //input 2
  pinMode(4, OUTPUT); //input 1
  pinMode(3,INPUT_PULLUP );
 
  
}

void loop()
{
  if (digitalRead(INPUT_PULLUP) == LOW)
  { //moving forward
  	digitalWrite(6, HIGH);
  	digitalWrite(7, LOW);
    analogWrite(10, 100);
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    analogWrite(11, 100); 
  }
  
}
