# Projetoiotarduino
Codigo para projeto de iot com Arduino/acender led com palmas
const byte ledPin = 8;
const byte soundPin = 9;
void setup()
{
  pinMode(ledPin, OUTPUT);
  pinMode(soundPin, INPUT);
}
void loop()
{
  readSound(); // detecta a presença de som
}

void readSound()
{
  if(digitalRead(soundPin))
  {  
    digitalRead(ledPin) ? digitalWrite(ledPin, LOW) : digitalWrite(ledPin, HIGH); // acende ou apaga o led
    delay(1000);
  }
