# Melody_buzzer.project

int melody[] = { 262, 294, 330, 349, 392, 440, 494, 523 };
const int buzzer = 8;
int noteDuration = 850;
int notedelay = 850;

void setup() {
  pinMode(buzzer, OUTPUT);
}

void loop() {
  delay(400);

  for (int i = 0; i < 8; i++) {
    tone(buzzer, melody[i], noteDuration);
    delay(noteDelay);
  }
  noTone(buzzer);
   delay (noteDelay);

  for (int j = 7; j >= 0; j--) {
    tone(buzzer, meldoy[j], noteDuration);
    delay(noteDelay);
  }

  if (noteDuration > 100) {
    noteDuration -= 150;
    noteDelay -= 150;
  } else {
    noteDuration = 850;
    noteDelay = 850;
  }
}
