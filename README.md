String[][] strs = new String[6][2];
PFont font;

void setup() {
  size(1920, 1080);
  font = createFont("HelveticaNeue-48.vlw", 48);
  textFont(font);
  frameRate(30);
  textAlign(CENTER);
  textSize(40);
  background(255);
  fill(0);

  strs[0][0] = "Bonjour!";
  strs[0][1] = "My name is Adithya Ramani.";

  strs[1][0] = "I'm a CA Final Student";
  strs[1][1] = "I am pursuing my articleship in Audit at Deloitte, India.";

  strs[2][0] = "I've been teaching myself how to code and trade for about 1 year. I am self-taught";
  strs[2][1] = "I work in Python and aspiring to learn PineScript";

  strs[3][0] = "I love to work in areas related finance and capital markets and see how they impact the economy in a large way.";
  strs[3][1] = "I would love to build finance related projects and bring a synergy between python and the capital markets";

  strs[5][0] = "If you like this page and want to support my work, you can buy me a coffee @;
  strs[5][1] = " [strike a chord](https://ko-fi.com/adithyaramani#paypalModal);
}

int i = 0;
boolean delete = false;
int s = 0;
int offset = 50;
int mainFontSize = 60;
int secondaryFontSize = 40;


void draw() {
  background(255);

  if (s < strs.length) {
    if ((strs[s][0].length() >= i || strs[s][1].length() >= i) && !delete) {
      if (strs[s][0].length() >= i) {
        textSize(mainFontSize);
        text(strs[s][0].substring(0, i), width/2, height/2 - offset);
      } else {
        textSize(mainFontSize);
        text(strs[s][0], width/2, height/2 - offset);
      }
      if (strs[s][1].length() >= i) {
        textSize(secondaryFontSize);
        text(strs[s][1].substring(0, i), width/2, height/2 + offset);
      } else {
        textSize(secondaryFontSize);
        text(strs[s][1], width/2, height/2 + offset);
      }
      i++;
    } else {
      if (!delete) {
        delay(1500);
      }
      delete = true;
    }


    if (delete) {

      if (i > 0) {
        if (i < strs[s][0].length()) {
          textSize(mainFontSize);
          text(strs[s][0].substring(0, i - 1), width/2, height/2 - offset);
        } else {
          textSize(mainFontSize);
          text(strs[s][0], width/2, height/2 - offset);
        }
        if (i < strs[s][1].length()) {
          textSize(secondaryFontSize);
          text(strs[s][1].substring(0, i - 1), width/2, height/2 + offset);
        } else {
          textSize(secondaryFontSize);
          text(strs[s][1], width/2, height/2 + offset);
        }
        i--;
      } else {
        delete = false;
        s++;
      }
    }
    //print(i + " ");
    //s++;
  }
}





![Bonjour!!! I'm Adithya Ramani. I'm interested in capital markets and its applications in python. Check out my work](https://github.com/Adithya-Ramani/Adithya-Ramani/raw/master/bio.gif)

I work as an audit associate at Deloitte, India.

Apart from Audit, i am passionate about financial and capital markets. I love to watch their movements and how they shape up the economy. 

I am a self-taught coder. I have learnt python on my own and aim to expand its applications into finance and the stock markets world. 

I am currently upskilling my levels at both python and the capital markets. I have built various finance related projects using python, the source codes is put in my repository.

We can collaborate on interesting projects in the field of Finance and capital markets.

Your can check my economics and mrarkets related blog page here [Econclave](https://econclave.digitalpress.blog/).
The contents of the blog is for open source, it can be used with attribution

If you really like my page and my work, buy me a coffee at [Strike a chord](https://ko-fi.com/adithyaramani#paypalModal)
