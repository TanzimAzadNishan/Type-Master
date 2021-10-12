/**     Type Master     **/

//  Submitted by :
//  Tanzim Azad Nishan     : 1705074
//  Md Emamul Haque Pranta : 1705078
//  Kazi Wasif Amin        : 1705079


# include "iGraphics.h"
#include <string.h>

#define _CRT_SECURE_NO_WARNINGS
# include <stdio.h>
# include <math.h>
# define N 300
# define PI 3.1415924
# include <Windows.h>
# include <MMSystem.h>

int wrd_speed = 20 ;

//high score

int hscore_para, hscore_bub, hscore_word, hscorewin = 999 ; //high score
FILE * hscore_ptr_para, * hscore_ptr_bub, * hscore_ptr_word;
char hs_para[5], hs_bub[5], hs_word[5] ;

int BUBBLE_SPEED = 2;//Easy mode

int bubx = 300, buby = 300, bubr = 20;
double bubcr=255,bubcg=255,bubcb=255;
int bubtimepassed=0,bubspeed=0,bubword=0,bubstate=0;
int bubmode=1,bubcounter=0;
double bubx1=100,bubx2=200;
double buby2=50,buby3=100;
char bubch[100][2],bubrem[3];
int bubcount[50]={0},bubscr=0;
char bubsp[2];
int bubindex=0,bubq,bubindexflag=3,bubidx=1;
char bubstr[100]="100",bubstrflag[100];
int bubcharacter=100;
char bubussc[5];
//int x = 300, y = 300, r = 20;
int window=0;
int wrd_x=0,wrd_t,wrd_p=200,wrd_q=60,wrd_r=110,wrd_n,wrd_k,wrd_colr=200,wrd_j;
int wrd_mode=0,wrd_i_idx=0,wrd_i_len=0,wrd_y=0,wrd_i=0;
char wrd_in_str[20]={0};
int wrd_md=0,wrd_z=0;
int wrd_stck,wrd_count=0,word_cnt=0;
int wrd_idx[5]={0},wrd_ix=0;
char wrd_ussc[5];
struct wrd_word
{
    char wrd_wrd[20];
};
struct wrd_word wrd_w[1000];


// *********   _____    ******** /

char word[N][40];

char b[100];

int timerINDEX ;

int idx = 0 , cur_min = 0;
int idx_temp = 0;
char str[50];
char ch[1];
int mark[300] = {0}, color_para_idx = -1;
int gid = 0, y;
int distance = 200;

int word_position = 0;


// **   Timer    **

char Time[2] ;
int timer = 60, timerTemp, var = 1 ;
double timer_red = 0.0, timer_green = 255.0;

// **   Timer    **

/**     Skipped     **/

char Skip[4] = "000" , skipped = 0, skipped_prev = 0, skipped_temp ;

/**     Skipped     **/


/** Correctness measurement **/

char correctness[3] ;

int correctWord = 0 ;
int correctRatio;
int typed = 0;

/** Correctness measurement **/


/** Score measurement **/

char scoreArray[6] = "00000";
int score = 0, scoreTemp;

/** Score measurement **/


/**     Speed Measurement    **/

double elapsed = 0;
int elapsed_temp = 0, word_typed = 0;
char Elapsed[3] ;
/**     Speed Measurement    **/


/**     Paragraph Sound     **/

//bool typeTone = false, type_word_failure = false ;

/**     Paragraph Sound     **/


/**     Background Sound     **/

//bool bgmusic = true;

/**     Background Sound     **/


/**     Difficulty     **/

int window_prev = 1 ;

//This determines for which game the level was called

/**     Difficulty     **/



void Return (void)
{
    /** WORD TRIS **/


    if (atoi(wrd_ussc) >= hscore_word)
    {
        hscore_word = atoi(wrd_ussc) ;
        fseek ( hscore_ptr_word, 0, SEEK_SET ) ;
        fprintf(hscore_ptr_word, "%d", hscore_word ) ;

        fseek (hscore_ptr_word, 0, SEEK_SET) ;
        fscanf (hscore_ptr_word, "%s", &hs_word) ;
    }


    wrd_x=0,wrd_t,wrd_p=200,wrd_q=60,wrd_r=110,wrd_n,wrd_k,wrd_colr=200,wrd_j;
    wrd_mode=0,wrd_i_idx=0,wrd_i_len=0,wrd_y=0,wrd_i=0;
    wrd_in_str[0]=0;
    wrd_md=0,wrd_z=0;
    wrd_stck,wrd_count=0,word_cnt=0;
    wrd_idx[0]=0,wrd_ix=0;
    wrd_ussc[0] = 0;

    /** WORD TRIS **/

    /** bubble **/

    BUBBLE_SPEED = 2;
    FILE* bubfp;
    int bubi;
	bubfp=fopen("word.txt","r");
	for(bubi=1;bubi<250;bubi++){
        fscanf(bubfp,"%s",bubch[bubi]);
	}
    fclose(bubfp);
     bubx = 300, buby = 300, bubr = 20;
     bubcr=255,bubcg=255,bubcb=255;
     bubtimepassed=0,bubspeed=0,bubword=0,bubstate=0;
     bubmode=1,bubcounter=0;
     bubx1=100,bubx2=200;
     buby2=50,buby3=100;
     bubch[100][2],bubrem[3];
    bubcount[50]={0},bubscr=0;
     bubsp[0] = '0' ;
     bubindex=0,bubq,bubindexflag=3,bubidx=1;
     bubstr[0]='1';
      bubstr[1]='0';
       bubstr[2]='0';
     //bubstrflag[100];
     bubcharacter=100;
     bubussc[0]='0';
     bubussc[1]='0';
     bubussc[2]='0';
     bubussc[3]='0';
     bubussc[4]='0';
    /** bubble **/


    /**     Paragraph    **/

    if (score >= hscore_para)
    {
        hscore_para = score ;
        fseek ( hscore_ptr_para, 0, SEEK_SET ) ;
        fprintf(hscore_ptr_para, "%d", hscore_para ) ;

        fseek (hscore_ptr_para, 0, SEEK_SET) ;
        fscanf (hscore_ptr_para, "%s", &hs_para) ;
    }

    b[0] = 0;

    idx = 0 , cur_min = 0;
    idx_temp = 0;
    str[0] = 0;

    for (int yy=0; yy<300; yy++)
        mark[yy] = 0;

    color_para_idx = -1;
    gid = 0;
    distance = 200;

    word_position = 0;


    // **   Timer    **

    //char Time[2] ;
    //timer = 60;
    timerTemp, var = 1 ;
    timer_red = 0.0, timer_green = 255.0;

    // **   Timer    **

    /**     Skipped     **/

    for (int Skip_i=0; Skip_i<strlen(Skip); Skip_i++)
        Skip[Skip_i] = '0' ;

    skipped = 0, skipped_prev = 0, skipped_temp ;

    /**     Skipped     **/


    /** Correctness measurement **/

   for (int correctness_i=0; correctness_i<strlen(correctness); correctness_i++)
        correctness[correctness_i] = 0 ;

    correctWord = 0 ;
    correctRatio;
    typed = 0;

    /** Correctness measurement **/


    /** Score measurement **/

    //char scoreArray[6] = "00000";
    for (int score_i=0; score_i<strlen(scoreArray); score_i++)
        scoreArray[score_i] = '0' ;

    score = 0, scoreTemp;

    /** Score measurement **/


    /**     Speed Measurement    **/

    elapsed = 0;
    elapsed_temp = 0, word_typed = 0;

    for (int Elapsed_i=0; Elapsed_i<strlen(Elapsed); Elapsed_i++)
        Elapsed[Elapsed_i] = 0 ;

    /**     Speed Measurement    **/


    /**     Paragraph   **/
}


void  wrd_clr(int wrd_n,char wrd_str[])
{
    int wrd_dx;
        for(wrd_dx=0;wrd_dx<wrd_n;wrd_dx++)
        {
            wrd_str[wrd_dx]='\0';
        }
}


void wrd_time()
{
    if(wrd_p<0)
    {
        wrd_p=250;
    }
    wrd_p-=20;
    if(wrd_q>=250)
    {
        wrd_q=0;
    }
    wrd_q+=20;
    if(wrd_r>=250)
    {
        wrd_r=0;
    }
    wrd_r+=20;

}
void wrd_curve()
{
    if(wrd_t>1000)
        wrd_t=900;

    wrd_t+=20;
}
void wrd_color()
{
    if(wrd_mode)
    {
        if(strcmp(wrd_in_str,wrd_w[wrd_i].wrd_wrd)==0)
        {
            PlaySound ("music\\type ok.wav", NULL, SND_ASYNC);
            wrd_y=0;
            wrd_i++;
            wrd_count++;
        }
        else if(wrd_y+wrd_stck>560)
      {
         PlaySound ("music\\type error.wav", NULL, SND_ASYNC);

        wrd_md++;wrd_idx[wrd_ix++]=wrd_i,wrd_i++;
        wrd_y=0;

        if(wrd_stck==160)
            wrd_mode=2;

        wrd_stck+=40;
       }

        else  wrd_y+=wrd_speed;
    }
     if(wrd_colr<0)
        wrd_colr=200;
       else
        wrd_colr-=20;

}

void wordtriswin(){
	//FIRST WINDOW
	if(!wrd_mode)
	{
        iSetColor(0,250,250);
        iFilledRectangle(0,0,1300,1000);
        iSetColor(0,255,250);
        iText(250,600,"WELCOME TO WORDTRIS",GLUT_BITMAP_TIMES_ROMAN_24);
        iSetColor(0,25,250);
        iText(50,420,"RULES:",GLUT_BITMAP_TIMES_ROMAN_24);
        iSetColor(300,00,250);
        iText(50,380,"1.YOU HAVE TO WRITE THE WORD ON THE TRIS BEFORE THEY STUCK TO THE GROUND.");
        iText(50,360,"2.YOU HAVE TO WRITE THE CORRECT WORD AT FIRST CHANCE IE. NO BACKSPACE IS ALLOWED.");
        iText(50,340,"3.AS SOON AS YOU WRITE A CORRET WORD THE TRIS AUTOMATICALLY VANISHES.");
        iSetColor(255,55,110);
        iText(50,310,"4.PRESS ENTER TO CLEAR WRITE DOWN BOX.",GLUT_BITMAP_HELVETICA_18);

//        iSetColor(255,255,0);
//        iFilledEllipse(400,500,80,30,1000);
//        iSetColor(0,0,0);
//        iText(360,490,"START",GLUT_BITMAP_TIMES_ROMAN_24);

        iShowBMP(320, 470, "bin//Debug//Start bubble.bmp") ;

	}


	if(wrd_mode==1)
    {
        iShowBMP(0, 0, "bin//debug//wordt.bmp");

        iSetColor(250,255,0);
        iFilledRectangle(280,90,240,60);

        iSetColor(300,300,300);
        word_cnt=wrd_count*5;
        bubscr=bubword*5;
        for(wrd_z=4;wrd_z>=0;wrd_z--){
            wrd_ussc[wrd_z]=(word_cnt%10)+48;
            word_cnt=word_cnt/10;
        }

        iSetColor(0, 0, 0) ;

        iText(140 ,420, "SCORE : ", GLUT_BITMAP_TIMES_ROMAN_24);

        iText(240,420,wrd_ussc,GLUT_BITMAP_TIMES_ROMAN_24);

        iText(315,110,wrd_in_str,GLUT_BITMAP_HELVETICA_18);
        // ornaments starts

       //boundary
       {
          iSetColor(0,255,255);
           iFilledRectangle(300,200,10,200);
            iFilledRectangle(500,200,10,200);
              iFilledRectangle(300,200,200,10);
       }
       //box sliding
       {

       iSetColor(30+wrd_colr,30,260-wrd_colr);
       iFilledRectangle(310,800-wrd_y,190,40);
       iSetColor(0,0,0);
       iText(350,815-wrd_y,wrd_w[wrd_i].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);

       }

       if(wrd_md>=1)
       {

           iSetColor(260,60,140);
            iFilledRectangle(310,210,190,40);
            iSetColor(0,0,0);
            iText(340,220,wrd_w[wrd_idx[0]].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);
       }
       if(wrd_md>=2)
       {

           iSetColor(320,120,80);
            iFilledRectangle(310,250,190,40);
            iSetColor(0,0,0);
            iText(340,260,wrd_w[wrd_idx[1]].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);

       }
        if(wrd_md>=3)
       {

           iSetColor(380,180,20);
            iFilledRectangle(310,290,190,40);
            iSetColor(0,0,0);
            iText(340,300,wrd_w[wrd_idx[2]].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);
       }
      if(wrd_md>=4)
       {

           iSetColor(400,240,0);
            iFilledRectangle(310,330,190,40);
            iSetColor(0,0,0);
            iText(340,340,wrd_w[wrd_idx[3]].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);
       }
       if(wrd_md>=5)
       {

           iSetColor(460,300,0);
            iFilledRectangle(310,370,190,40);
            iSetColor(0,0,0);
            iText(340,380,wrd_w[wrd_idx[4]].wrd_wrd,GLUT_BITMAP_TIMES_ROMAN_24);
       }


}
     if(wrd_mode==2)
     {
         iShowBMP(0, 0,"bin//Debug//reto.bmp");
        //iSetColor(250,250,0);
        //iFilledRectangle(300,400,400,200);
        iSetColor(255,255,250);
        iText(320,350,"GAME OVER !!!!",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(320, 300,"Score :",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(430, 300, wrd_ussc , GLUT_BITMAP_TIMES_ROMAN_24) ;


        wrd_x=0,wrd_t,wrd_p=200,wrd_q=60,wrd_r=110,wrd_n,wrd_k,wrd_colr=200,wrd_j;
        wrd_i_idx=0,wrd_i_len=0,wrd_y=0,wrd_i=0;
        wrd_in_str[0]=0;
        wrd_md=0,wrd_z=0;
        wrd_stck,wrd_count=0,word_cnt=0;
        wrd_idx[0]=0,wrd_ix=0;

     }
}

void bubble(double buby1)
{
    int bubp;
    int bubi,bubj,bubk,bubn=1,bubflag=1;
    for(bubi=1;bubi<=(bubcharacter/3)+1;bubi++){
        if(bubi%2==1){
            bubx1=100;
        }
        else{
            bubx1=200;
        }
        for(bubj=1;bubj<=3;bubj++){
            if((bubi*bubj)%6==1) {bubcr=255; bubcg=155; bubcb=135;}
            if((bubi*bubj)%6==2) {bubcr=255; bubcg=75; bubcb=175;}
            if((bubi*bubj)%6==3) {bubcr=186; bubcg=127; bubcb=70;}
            if((bubi*bubj)%6==4) {bubcr=0; bubcg=255; bubcb=255;}
            if((bubi*bubj)%6==5){bubcr=0; bubcg=25; bubcb=255;}
            if((bubi*bubj)%6==6){bubcr=128; bubcg=255; bubcb=255;}
            bubflag=1;
            bubn++;
            if(bubn>bubcharacter+1)
                goto bubx;
            for(bubk=0;bubk<bubcharacter+1;bubk++){
                if((bubn-1)==bubcount[bubk]){
                    bubflag=0;
                    break;
                }
            }
            if(bubflag==1){
                if(buby1<=1000){
                iSetColor(bubcr,bubcg,bubcb);
                iFilledCircle(bubx1,buby1,25);
                iSetColor(0,0,0);
                iText(bubx1-5,buby1-5,bubch[bubn-1],GLUT_BITMAP_TIMES_ROMAN_24);
                }
                else{
                    bubch[bubn-1][0]='\0';
                }
            }
            bubx1=bubx1+200;
        }
        buby1=buby1-100;
    }
    bubx:
        bubp=0;
}

void bubbleproduce(){
    bubble(buby2);
}

void bubmove(){
    if(bubmode==2)
    {
        buby2=buby2+BUBBLE_SPEED;
        bubble(buby2);
    }

    if(buby2-(bubcharacter/3)*100>=1000)
    {
      bubmode=3;
    }

    bubble(buby2);
}

void bubtime(){
    if(bubmode==2){
        bubtimepassed++;
    }
}
void bubblewin()
{
	if(bubmode==1)
    {
        iShowBMP(0, 0, "bin//Debug//water.bmp") ;

        if(bubcounter==1)
        {
            iSetColor(0,0,0);
            iText(335, 595, bubstr, GLUT_BITMAP_TIMES_ROMAN_24);
        }

        if(bubcounter==0)
        {
            iSetColor(0, 0, 255);
            iFilledRectangle(330,590,50,30);
        }

        iSetColor(0,0,0);
        iText(335, 595, bubstr, GLUT_BITMAP_TIMES_ROMAN_24);
        iSetColor(200, 20, 200);
        iText(100, 600, "Total Characters",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(100, 300, "type every character before they vanish",GLUT_BITMAP_TIMES_ROMAN_24);
        iRectangle(325,575,75,50);

        iShowBMP(590, 80, "bin//Debug//Start bubble.bmp") ;
	}

	if(bubmode==2)
    {
        //PlaySound ("music//bubble up.wav", NULL, SND_ASYNC) ;

        iShowBMP(0, 0, "bin//Debug//water.bmp") ;

        iSetColor(20, 200, 200);
        iSetColor(0,0,0);
        bubbleproduce();
	}

	if(bubword==bubcharacter){
        bubmode=3;
	}

	if(bubmode==3){

         //PlaySound ("music//bubble up.wav", NULL, SND_ASYNC) ;

        iShowBMP(0, 0, "bin//Debug//water.bmp") ;
        bubscr=bubword*5;

        int bubscore = bubscr ;

        for(bubq=4;bubq>=0;bubq--){
            bubussc[bubq]=(bubscr%10)+48;
            bubscr=bubscr/10;
        }
        bubspeed=bubword/bubtimepassed;
        bubsp[0]=bubspeed+48;
        bubr=bubcharacter-bubword;
        for(bubq=2;bubq>=0;bubq--){
            bubrem[bubq]=((bubr)%10)+48;
            bubr=(bubr)/10;
        }
        iSetColor(0,0,0);
        iText(100,700,"speed=",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(100,600,"score=",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(200,600,bubussc,GLUT_BITMAP_TIMES_ROMAN_24);
        iText(100,400,"character remained=",GLUT_BITMAP_TIMES_ROMAN_24);
        iText(400,400,bubrem,GLUT_BITMAP_TIMES_ROMAN_24);
        iText(180,698,bubsp,GLUT_BITMAP_TIMES_ROMAN_24);
        iText(200,700,"character/sec",GLUT_BITMAP_TIMES_ROMAN_24);

        //printf("\n\t HS = %d\n", atoi (bubussc)) ;

        //int bub_score = atoi (bubussc) ;

        if ( bubscore >= hscore_bub )
        {
            iText(200,500,"CONGRATS ! HIGH SCORE !!",GLUT_BITMAP_TIMES_ROMAN_24);
            hscore_bub = bubscore ;
            fseek ( hscore_ptr_bub, 0, SEEK_SET ) ;
            fprintf(hscore_ptr_bub, "%d", hscore_bub ) ;
            fscanf (hscore_ptr_bub, "%s", &hs_bub) ;
        }

        else
        {
            iText(200,500,"HIGH SCORE : ",GLUT_BITMAP_TIMES_ROMAN_24);
            iText(420,500,hs_bub,GLUT_BITMAP_TIMES_ROMAN_24);
        }
	}
}

/**     Speed Measurement    **/


void Speed(void)
{
    elapsed += 0.1 ;
}


void Time_minute(void)
{
    cur_min += 20;

    /**     Skipped     **/

    skipped_prev = (20 * var) - idx ;
    skipped += skipped_prev ;

    skipped_temp = skipped ;

    Skip[2] = skipped_temp % 10 + 48 ;
    skipped_temp /= 10;
    Skip[1] = skipped_temp % 10 + 48 ;
    skipped_temp /= 10;

    if (skipped_temp == 0)
        Skip[0] = ' ' ;
    else
        Skip[0] = skipped_temp % 10 + 48;

    /**     Skipped     **/

    idx = 20 * var;
    color_para_idx = (20 * var - 1);
    timer = 60;
    timer_red = 0.0 ;
    timer_green = 255.0;

    var++;
}


void Clock(void)
{
    timer--;
    timer_red += 4.25 ;
    timer_green -= 4.25;

                if (timer <= 0)
                {
                    cur_min += 20;

                    /**     Skipped     **/

                    skipped_prev = (20 * var) - idx ;
                    skipped += skipped_prev ;

                    skipped_temp = skipped ;

                    Skip[2] = skipped_temp % 10 + 48 ;
                    skipped_temp /= 10;
                    Skip[1] = skipped_temp % 10 + 48 ;
                    skipped_temp /= 10;

                    if (skipped_temp == 0)
                        Skip[0] = ' ' ;
                    else
                        Skip[0] = skipped_temp % 10 + 48;

                    /**     Skipped     **/

                    idx = 20 * var;
                    color_para_idx = (20 * var - 1);
                    timer = 60;
                    timer_red = 0.0 ;
                    timer_green = 255.0;

                    var++;

                }
}

void paragraphwin()
{
    iShowBMP(0, 0, "bin//Debug//aurora.bmp");

    /**     TIMER       **/

    iSetColor(timer_red, timer_green, 0);

    iFilledCircle(100, 100, 50);

    iSetColor(0, 0, 0);
    iFilledCircle(100, 100, 40);

    timerTemp = timer;
    Time[1] = timerTemp % 10 + 48 ;
    timerTemp /= 10;
    Time[0] = timerTemp % 10 + 48 ;

    iSetColor(timer_red, timer_green, 0);
    iText (88.5, 92, Time, GLUT_BITMAP_TIMES_ROMAN_24);

    /**     TIMER       **/

    iSetColor(255, 255, 255) ;

    iText(50, 630, "          Score : ", GLUT_BITMAP_TIMES_ROMAN_24);
    iText(190, 630, scoreArray, GLUT_BITMAP_TIMES_ROMAN_24);

    iText(50, 600, "Correctness : ", GLUT_BITMAP_TIMES_ROMAN_24);
    iText(190, 600, correctness, GLUT_BITMAP_TIMES_ROMAN_24);
    iText(250, 600, "%", GLUT_BITMAP_TIMES_ROMAN_24);

    iText(50, 570, "          Speed : ", GLUT_BITMAP_TIMES_ROMAN_24);
    iText(190, 570, Elapsed, GLUT_BITMAP_TIMES_ROMAN_24);
    iText(250, 570, "word/min", GLUT_BITMAP_TIMES_ROMAN_24);

    iText(50, 540, "        Skipped : ", GLUT_BITMAP_TIMES_ROMAN_24);
    iText(190, 540, Skip, GLUT_BITMAP_TIMES_ROMAN_24);

    word_position = 0;
    distance = 200;

    iSetColor(255, 255, 255);
    iRectangle(500, 200, 300, 60);

    for (y=0; y<10; y++)
    {
        if ((y+cur_min) <= color_para_idx)
        {
            if (mark[y+cur_min] == 1)
                iSetColor(255, 0, 0);

            else
                iSetColor(0, 255, 0);
        }

        else
            iSetColor(15, 178, 230);

        iText(distance+word_position, 400, word[y+cur_min], GLUT_BITMAP_TIMES_ROMAN_24);

        word_position = word_position + strlen(word[y+cur_min]) * 12 + 13;
     }

    distance = 200;
    word_position = 0;

    for (y=10,gid=0; y<20 || gid<10; y++, gid++)
    {
        if ((y+cur_min) <= color_para_idx)
        {
            if (mark[y+cur_min] == 1)
                iSetColor(255, 0, 0);

            else
                iSetColor(0, 255, 0);
        }

        else
            iSetColor(15, 178, 230);

        iText(distance+word_position, 350, word[y+cur_min], GLUT_BITMAP_TIMES_ROMAN_24);

        word_position = word_position + strlen(word[y+cur_min]) * 14 + 10;
    }

    iSetColor(255, 255, 255);
    iText(510, 215, str, GLUT_BITMAP_TIMES_ROMAN_24);

    iSetColor(0, 255, 255);
    iText(190, 160, "Type Every word. As soon as you press space, no correction is possible.", GLUT_BITMAP_TIMES_ROMAN_24);
}

void iDraw()
{
	iClear();

    if (window == hscorewin )
    {
        iShowBMP(0,0, "bin//debug//sheep.bmp");
        iText (760, 607, hs_para, GLUT_BITMAP_TIMES_ROMAN_24 ) ;
        iText (760, 515, hs_bub, GLUT_BITMAP_TIMES_ROMAN_24 ) ;
        iText (760, 424, hs_word, GLUT_BITMAP_TIMES_ROMAN_24 ) ;
    }

	if (window == 0)
    {
        iShowBMP(0,0, "bin//debug//window 0.bmp");
    }

    if(window==4)
    {
        paragraphwin();
	}

	if (window == 6)
    {
        iShowBMP(0,0, "bin//Debug//Difficulty.bmp") ;
    }

	if(window==1)
    {
	    iShowBMP(0,0, "bin//debug//window 1 2.bmp");
	}

	if(window==2)
    {
        bubblewin();
	}

    if(window==3)
    {
        wordtriswin();
	}

	if(window == 1)
    {
        Return();
    }

    if (window != 0 && window != 1)
    {
        iShowBMP(1000, 100, "bin//Debug//main menu.bmp");
    }
}

/*
	function iMouseMove() is called when the user presses and drags the mouse.
	(mx, my) is the position where the mouse pointer is.
	*/
void iMouseMove(int mx, int my)
{
    printf("\tmx = %d, my = %d\n", mx, my);
}


void iMouse(int button, int state, int mx, int my)
{
	if (button == GLUT_LEFT_BUTTON && state == GLUT_DOWN)
    {
        PlaySound("music\\click2.wav", NULL, SND_ASYNC);

        if (window != 0 && window != 1)
        {
            if (mx >=990 && mx <= 1210 && my >=98 && my <= 155)
            {
                Return() ;
                window = 1;
                window_prev = 1;
                PlaySound(0, 0, 0) ;
                PlaySound("music\\click2.wav", NULL, SND_ASYNC);
                //PlaySound ("music\\bgg.wav", NULL, SND_ASYNC);
            }
        }

        else if (window == 0)
        {
            if (mx >=553 && mx <= 736 && my >=230 && my <= 336)
            {
                window = 1;
                //PlaySound ("music\\bgg.wav", NULL, SND_ASYNC);
            }
        }

        if(window == 1)
        {
            if(my<=905 && my>=855 && mx>=989 && mx<=1208)
            {
                //paragraphwin() ;

                window = 4 ;
            }

            else if(mx<=1208 && mx>=1036 && my>=760 && my<=815)
            {
                //bubblewin() ;

                window = 2 ;
            }

            else if(mx<=1208 && mx>=1000 && my>=656 && my<=709)
            {
                //wordtriswin() ;

                window = 3;
            }

            else if(mx<=1211 && mx>=1000 && my>=572 && my<=627)
            {
                //wordtriswin() ;

                window = hscorewin;
            }

            if(mx<=218 && mx>=76 && my>=249 && my<=298)
            {
                //paragraphwin() ;

                exit (0) ;
            }
        }

        if(window==2 && window_prev == 1)
        {
            window_prev = 2;
            window = 6;
        }

        if(window==3 && window_prev == 1)
        {

            window_prev = 3;
            window = 6;
        }
        if(window==4 && window_prev == 1){

                window_prev = 4;
                window = 6;

            if(mx>=100 && mx<=620 && my<=510 && my>=450){
                 b[0] = 0;
            }
        }

        if (window == 6)
        {
            if (mx >= 735 && mx <= 868 && my >=638 && my <= 680 )
            {
                //Easy

                /**     Paragraph    **/

                if (window_prev == 4)
                {
                    PlaySound("music//tickk.wav", NULL, SND_LOOP | SND_ASYNC) ;
                    window = 4;

                    timer = 60 ;

                    FILE * fp ;

                    fp = fopen ("Dic easy.txt", "r");

                    for (int i=0; i<N; i++)
                    {
                        fscanf(fp, "%s", word[i]);
                        fflush(stdin);
                    }

                    fclose(fp);

                    /**     Paragraph    **/

                    b[0] = 0;

                    idx = 0 , cur_min = 0;
                    idx_temp = 0;
                    str[0] = 0;
                    mark[150] = {0}, color_para_idx = -1;
                    gid = 0;
                    distance = 200;

                    word_position = 0;


                    // **   Timer    **

                    //char Time[2] ;
                    timer = 60, timerTemp, var = 1 ;
                    timer_red = 0.0, timer_green = 255.0;

                    // **   Timer    **

                    /**     Skipped     **/

                    skipped = 0, skipped_prev = 0, skipped_temp ;

                    /**     Skipped     **/


                    /** Correctness measurement **/;

                    correctWord = 0 ;
                    correctRatio;
                    typed = 0;

                    /** Correctness measurement **/


                    /** Score measurement **/

                    //char scoreArray[6] = "00000";
                    score = 0, scoreTemp;

                    /** Score measurement **/


                    /**     Speed Measurement    **/

                    elapsed = 0;
                    elapsed_temp = 0, word_typed = 0;

                    /**     Speed Measurement    **/


                    /**     Paragraph   **/
                }

                /**     Paragraph    **/


                /**     Bubble    **/

                else if (window_prev == 2)
                {
                    window = 2;
                    BUBBLE_SPEED = 3 ;
                }

                /**     Bubble    **/


                /**     Word Tris    **/

                else if (window_prev == 3)
                {
                    window = 3;

                    wrd_speed = 15;

                    FILE *wrd_f;
                    wrd_f=fopen("Dict_Easy.txt","r");
                    for(int i=0;i<1000;i++)
                    {
                       fscanf(wrd_f,"%s",wrd_w[i].wrd_wrd);
                    }
                    fclose(wrd_f);
                }

                /**     Word Tris    **/
            }

            else if ( mx >= 766 && mx <= 937 && my >=570 && my <= 617 )
            {
                //Medium


                /**     Paragraph    **/

                if (window_prev == 4)
                {
                    window = 4;
                    timer = 60 ;
                    PlaySound("music//tickk.wav", NULL, SND_LOOP | SND_ASYNC) ;

                    FILE * fp ;

                    fp = fopen ("Dict_Medium_2.txt", "r");

                    for (int i=0; i<N; i++)
                    {
                        fscanf(fp, "%s", word[i]);
                        fflush(stdin);
                    }

                    fclose(fp);

                    b[0] = 0;

                    idx = 0 , cur_min = 0;
                    idx_temp = 0;
                    str[0] = 0;
                    mark[150] = {0}, color_para_idx = -1;
                    gid = 0;
                    distance = 200;

                    word_position = 0;


                    // **   Timer    **

                    //char Time[2] ;
                    timer = 60, timerTemp, var = 1 ;
                    timer_red = 0.0, timer_green = 255.0;

                    // **   Timer    **

                    /**     Skipped     **/

                    skipped = 0, skipped_prev = 0, skipped_temp ;

                    /**     Skipped     **/


                    /** Correctness measurement **/;

                    correctWord = 0 ;
                    correctRatio;
                    typed = 0;

                    /** Correctness measurement **/


                    /** Score measurement **/

                    //char scoreArray[6] = "00000";
                    score = 0, scoreTemp;

                    /** Score measurement **/


                    /**     Speed Measurement    **/

                    elapsed = 0;
                    elapsed_temp = 0, word_typed = 0;

                    /**     Speed Measurement    **/


                    /**     Paragraph   **/
                }

                /**     Paragraph    **/



                /**     Bubble    **/

                else if (window_prev == 2)
                {
                    window = 2;
                    BUBBLE_SPEED = 6 ;
                }

                /**     Bubble    **/


                /**     Word Tris    **/

                else if (window_prev == 3)
                {
                    window = 3;
                    wrd_speed = 18 ;

                    FILE *wrd_f;
                    wrd_f=fopen("Dict_mid.txt","r");
                    for(int i=0;i<1000;i++)
                    {
                       fscanf(wrd_f,"%s",wrd_w[i].wrd_wrd);
                    }
                    fclose(wrd_f);
                }

                /**     Word Tris    **/


            }

            else if ( mx >= 800 && mx <= 965 && my >=502 && my <= 547 )
            {
                //Difficult


                /**     Paragraph    **/

                if (window_prev == 4)
                {
                    window = 4;
                    timer = 60 ;
                    PlaySound("music//tickk.wav", NULL, SND_LOOP | SND_ASYNC) ;

                    FILE * fp ;

                    fp = fopen ("Dict_Difficult.txt", "r");

                    for (int i=0; i<N; i++)
                    {
                        fscanf(fp, "%s", word[i]);
                        fflush(stdin);
                    }

                    fclose(fp);

                    b[0] = 0;

                    idx = 0 , cur_min = 0;
                    idx_temp = 0;
                    str[0] = 0;
                    mark[150] = {0}, color_para_idx = -1;
                    gid = 0;
                    distance = 200;

                    word_position = 0;


                    // **   Timer    **

                    //char Time[2] ;
                    timer = 60, timerTemp, var = 1 ;
                    timer_red = 0.0, timer_green = 255.0;

                    // **   Timer    **

                    /**     Skipped     **/

                    skipped = 0, skipped_prev = 0, skipped_temp ;

                    /**     Skipped     **/


                    /** Correctness measurement **/;

                    correctWord = 0 ;
                    correctRatio;
                    typed = 0;

                    /** Correctness measurement **/


                    /** Score measurement **/

                    //char scoreArray[6] = "00000";
                    score = 0, scoreTemp;

                    /** Score measurement **/


                    /**     Speed Measurement    **/

                    elapsed = 0;
                    elapsed_temp = 0, word_typed = 0;

                    /**     Speed Measurement    **/


            /**     Paragraph   **/

                }

                /**     Paragraph    **/



                /**     Bubble    **/

                else if (window_prev == 2)
                {
                    window = 2;
                    BUBBLE_SPEED = 8 ;
                }

                /**     Bubble    **/


                /**     Word Tris    **/

                else if (window_prev == 3)
                {
                    window = 3;
                    wrd_speed = 21 ;

                    FILE *wrd_f;
                    wrd_f=fopen("Dict_diff.txt","r");
                    for(int i=0;i<1000;i++)
                    {
                       fscanf(wrd_f,"%s",wrd_w[i].wrd_wrd);
                    }
                    fclose(wrd_f);
                }

                /**     Word Tris    **/

            }
        }


        if ( window == 2 )
        {
            if((mx >= 325 && mx <= 400) && (my <= 625 && my >= 575))
            {
                bubcounter=1;
                bubmode=1;
            }

            if(mx>=590 && mx<=780 && my>=80 && my<=530)
            {
                bubmode=2;
                PlaySound("music//bubble.wav", NULL, SND_ASYNC) ;
            }
        }

        else if (window == 3)
        {
            if(mx<480 && mx>320 && my<530 && my>480)
            {
                wrd_mode=1;
            }

            if(wrd_mode==2)
            {
                if(mx>200&&mx<500&&my>100&&my<140)
                {
                    wrd_mode=0;
                }
            }
        }

        else if (window == 4)
        {

        }
	}

}

/*
	function iKeyboard() is called whenever the user hits a key in keyboard.
	key- holds the ASCII value of the key pressed.
	*/
void iKeyboard(unsigned char key) {
    int bubi,bubj;
    if(window==2){
        if(bubmode==1){
            if(bubcounter==1){
                if (key != '\b'){
                    bubstr[bubindexflag]=key;
                    bubstr[bubindexflag+1]='\0';
                    bubindexflag++;
                }

                else{
                    if (bubindexflag >= 0){
                        bubstr[bubindexflag-1]='\0';
                        bubindexflag--;
                    }
                    else{
                        bubindexflag = 0;
                    }
                }
            }
            if(strlen(bubstr)==3){
                bubcharacter=(bubstr[0]-48)*100+(bubstr[1]-48)*10+(bubstr[2]-48);
            }
            if(strlen(bubstr)==2){
                bubcharacter=(bubstr[0]-48)*10+(bubstr[1]-48);
            }
            if(strlen(bubstr)==1){
                bubcharacter=bubstr[0]-48;
            }

        }

        if(bubmode==2){
            if(key!='\b'){
               for(bubi=1;bubi<bubcharacter+1;bubi++){
                    if(bubch[bubi][0]==key){
                        bubch[bubi][0]='\0';
                        PlaySound ("music\\Balloon.wav", NULL, SND_ASYNC) ;
                        bubcount[bubi]=bubi;
                        bubword++;
                        break;
                    }
               }
            }
        }
    }

    if(window==3)
    {

        if(key=='\r')
        {
            wrd_clr(wrd_i_len,wrd_in_str);
            wrd_i_idx=0;

            wrd_i_len=0;
        }
        else
        {
            PlaySound ("music\\stroke3.wav", NULL, SND_ASYNC);

           wrd_in_str[wrd_i_idx++]=key;
           // out_str[o_idx++]=key;
            wrd_i_len++;
            if(wrd_i_len>=16)
            {
                key='\r';
            wrd_clr(wrd_i_len,wrd_in_str);
            wrd_i_idx=0;

            wrd_i_len=0;
            }
        }
    }

    if(window==4){
        if (key == ' ')
        {
            typed++;

            /**     Speed Measurement   **/

            if ( str[0] != 0 )
                word_typed++;

            elapsed_temp = (int) ( word_typed * 60.0 / elapsed ) ;

            Elapsed[2] = elapsed_temp % 10 + 48 ;
            elapsed_temp /= 10;
            Elapsed[1] = elapsed_temp % 10 + 48 ;
            elapsed_temp /= 10;

            if (elapsed_temp == 0)
                Elapsed[0] = ' ';
            else
                Elapsed[0] = elapsed_temp + 48 ;

            /**     Speed Measurement   **/

            if (idx < (20 * var))
            {
                if ( strcmp(str, word[idx]) == 0 )
                {
                    PlaySound ("music\\type ok.wav", NULL, SND_ASYNC);

                    color_para_idx++;

                    correctWord++ ;
                    score += strlen (str);

                    idx++ ;
                }

                else
                {
                    color_para_idx++;
                    mark[idx] = 1;

                    PlaySound ("music\\type error.wav", NULL, SND_ASYNC);

                    idx++ ;
                }
            }

            if (idx == 20 * var)
            {
                cur_min += 20;

                /**     Skipped     **/

                skipped_prev = (20 * var) - idx ;
                skipped += skipped_prev ;

                skipped_temp = skipped ;

                Skip[2] = skipped_temp % 10 + 48 ;
                skipped_temp /= 10;
                Skip[1] = skipped_temp % 10 + 48 ;
                skipped_temp /= 10;

                if (skipped_temp == 0)
                    Skip[0] = ' ' ;
                else
                    Skip[0] = skipped_temp % 10 + 48;

                /**     Skipped     **/

                idx = 20 * var;
                color_para_idx = (20 * var - 1);
                timer = 60;
                timer_red = 0.0 ;
                timer_green = 255.0;

                var++;
            }

            str[0] = 0;

            /** Correctness Measurement **/

                correctRatio =  (int)  ( ( (double) correctWord / (double) (typed) * 100 ) ) ;
                correctness[2] = (correctRatio % 10) + 48;
                correctRatio /= 10;
                correctness[1] = (correctRatio % 10) + 48;
                correctRatio /= 10;

                if (correctRatio != 0)
                    correctness[0] = '1';
                else
                    correctness[0] = ' ' ;

            /** Score Measurement   **/
                scoreTemp = score;
                scoreArray[4] = (scoreTemp % 10) + 48 ;
                scoreTemp /= 10;
                scoreArray[3] = (scoreTemp % 10) + 48 ;
                scoreTemp /= 10;
                scoreArray[2] = (scoreTemp % 10) + 48 ;
                scoreTemp /= 10;
                scoreArray[1] = (scoreTemp % 10) + 48 ;
                scoreTemp /= 10;
                scoreArray[0] = (scoreTemp % 10) + 48 ;
        }

        else if (key == '\b')
        {
            PlaySound ("music\\stroke3.wav", NULL, SND_ASYNC);

            if (str[strlen(str)-1] != 32)
                str[strlen(str)-1] = 0;
        }

        else if (key != '\r')
        {
            ch[0] = key;
            strcat(str, ch);

            //typeTone = true;

            //if ( typeTone )
                PlaySound ("music\\stroke3.wav", NULL, SND_ASYNC);

            //typeTone = false;
                //PlaySound (0, 0, 0);
        }
    }

	if (key == '\0')
    {
		exit(0);
	}
	//place your codes for other keys here
}

/*
	function iSpecialKeyboard() is called whenver user hits special keys like-
	function keys, home, end, pg up, pg down, arraows etc. you have to use
	appropriate constants to detect them. A list is:
	GLUT_KEY_F1, GLUT_KEY_F2, GLUT_KEY_F3, GLUT_KEY_F4, GLUT_KEY_F5, GLUT_KEY_F6,
	GLUT_KEY_F7, GLUT_KEY_F8, GLUT_KEY_F9, GLUT_KEY_F10, GLUT_KEY_F11, GLUT_KEY_F12,
	GLUT_KEY_LEFT, GLUT_KEY_UP, GLUT_KEY_RIGHT, GLUT_KEY_DOWN, GLUT_KEY_PAGE UP,
	GLUT_KEY_PAGE DOWN, GLUT_KEY_HOME, GLUT_KEY_END, GLUT_KEY_INSERT
	*/
void iSpecialKeyboard(unsigned char key) {

	if (key == GLUT_KEY_END) {
		exit(0);
	}
	//place your codes for other keys here
}


int main()
{
	FILE* bubfp;

    int i = 0, j;
	int bubi;
	bubfp=fopen("word.txt","r");
	for(bubi=1;bubi<250;bubi++){
        fscanf(bubfp,"%s",bubch[bubi]);
	}
    fclose(bubfp);

    hscore_ptr_para = fopen ("High Score Para.txt", "r+") ;
    hscore_ptr_bub = fopen ("High Score Bub.txt", "r+") ;
    hscore_ptr_word = fopen ("High Score Word.txt", "r+") ;

    fscanf (hscore_ptr_para, "%d", &hscore_para) ;
    fscanf (hscore_ptr_bub, "%d", &hscore_bub) ;
    fscanf (hscore_ptr_word, "%d", &hscore_word) ;

    fseek (hscore_ptr_para, 0, SEEK_SET) ;
    fseek (hscore_ptr_bub, 0, SEEK_SET) ;
    fseek (hscore_ptr_word, 0, SEEK_SET) ;

    fscanf (hscore_ptr_para, "%s", &hs_para) ;
    fscanf (hscore_ptr_bub, "%s", &hs_bub) ;
    fscanf (hscore_ptr_word, "%s", &hs_word) ;

    iSetTimer(1000, Clock);
    iSetTimer(100, Speed);


    iSetTimer(100,wrd_time);
    iSetTimer(200,wrd_color);
    iSetTimer(200,wrd_curve);
    iSetTimer(10,bubmove);
    iSetTimer(1000,bubtime);
	iInitialize(1300, 1000, "TYPE MASTER");
	return 0;
}
