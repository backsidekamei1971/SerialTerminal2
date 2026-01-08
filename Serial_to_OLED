#define OLED_DATA 9
#define OLED_CLK 10
#define OLED_DC 11
#define OLED_CS 12
#define OLED_RST 13

#include <SSD1306ASCII.h>

SSD1306ASCII oled(OLED_DATA, OLED_CLK, OLED_DC, OLED_RST, OLED_CS);

int incomingByte = 0; // for incoming serial data


String ccc;
int row=0;

void setup() {
  Serial.begin(9600); // opens serial port, sets data rate to 9600 bps

   oled.ssd1306_init(SSD1306_SWITCHCAPVCC);
  
  oled.clear();
  oled.println("Hello world!");  
}

void loop() {
  // reply only when you receive data:
 
  if (Serial.available() > 0) {
    // read the incoming byte:
    //incomingByte = Serial.read();
    row=row+1;
    String ccc;
    ccc=Serial.readString();
    // say what you got:
    //Serial.println("I received: ");
    //Serial.println(incomingByte, DEC);
    //oled.print(incomingByte);
    Serial.print(ccc);
  //oled.clear();
  oled.setCursor(0, row);
    oled.println(ccc);
    oled.println("\n");
    //oled.scroll();
   
  }
}
