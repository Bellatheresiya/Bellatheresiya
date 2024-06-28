//program contoh pengenalan angka desimal MK SC Klp. E13.401

#termasuk <iostream.h>

#sertakan <stdlib.h>

#sertakan <conio.h>

#termasuk <stdio.h>

/* proses acak */

mengapung d_rand(void)

{

    kembali((float)(rand()%32767)/32767.0-0.5*2.0);

}

utama()

{

   ke dalam i,j,p,l,keluar[10],ERR[10],jum;

   int x[10][8]={{1,1,1,1,1,1,0,1},

                 {0,1,1,0,0,0,0,1},

                 {1,1,0,1,1,0,1,1},

                 {1,1,1,1,0,0,1,1},

                 {0,1,1,0,0,1,1,1},

                 {1,0,1,1,0,1,1,1},

                 {0,0,1,1,1,1,1,1},

                 {1,1,1,0,0,0,0,1},

                 {1,1,1,1,1,1,1,1},

                 {1,1,1,0,0,1,1,1}};

   ke dalam T[10][10]={{1,0,0,0,0,0,0,0,0,0},

                  {0,1,0,0,0,0,0,0,0,0,0},

                  {0,0,1,0,0,0,0,0,0,0,0},

                  {0,0,0,1,0,0,0,0,0,0},

                  {0,0,0,0,1,0,0,0,0,0},

                  {0,0,0,0,0,1,0,0,0,0},

                  {0,0,0,0,0,0,1,0,0,0},

                  {0,0,0,0,0,0,0,1,0,0},

                  {0,0,0,0,0,0,0,0,1,0},

                  {0,0,0,0,0,0,0,0,0,1}};

   float w[10][8],O[10],LR=0,1, init=0,15,kesalahan;
//inisialisasi bobot

   untuk (j=0;j<10;j++)

   {

      untuk (i=0;i<8;i++)

      {

         w[j][i]=init*d_rand();

      }

   }

   //pelatihan

   untuk(l=0;l<100;l++)

   {

   kesalahan=0,0; jum=1;

   untuk (p=0;p<10;p++)

   {

      untuk (j=0;j<10;j++)

      {

        HAI[j]=0,0;

        untuk (i=0;i<8;i++)

        {

          Bahasa Indonesia: O[j]=O[j]+x[p][i]*w[j][i];

        }

        jika(O[j]>0.0)

            keluar[j]=1;

        kalau tidak

             keluar[j]=0;

        ERR[j]=T[p][j]-keluar[j];

        kesalahan=kesalahan+abs(ERR[j]);

        jum++;

        jika(ERR[j]!=0)

        {

         untuk(i=0;i<8;i++)

         {

             w[j][i]=w[j][i]+LR*x[p][i]*ERR[j];

         }

        }

      }

   }

   kesalahan=kesalahan/jum;

   cout<<" l :"<<l<<" kesalahan : "<<kesalahan<<endl;

   }

//berlari

   untuk (i=0;i<7;i++)

   {

      cout<<"X"<<i+1<<":";

      cin>>x[0][i];

   }

   untuk (j=0;j<10;j++)

   {

     O[j]=0,0;

     untuk(i=0;i<8;i++)

     {

        Bahasa Indonesia: O[j]=O[j]+x[0][i]*w[j][i];

     }

     jika(O[j]>0.0)

         keluar[j]=1;

     kalau tidak

         keluar[j]=0;

     cout<<O[j]<<endl;

   }

jika((keluar[0]==1)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0 )&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 0"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==1)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 1"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==1)&&(keluar[3]==0)&&(keluar[4]==0 )&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 2"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==1)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 3"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==1)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 4"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==1)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 5"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==1)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 6"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==1)&&(keluar[8]==0)&&(keluar[9]==0))

      cout<<"Keluaran = 7"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==1)&&(keluar[9]==0))

      cout<<"Keluaran = 8"<<endl;

   jika((keluar[0]==0)&&(keluar[1]==0)&&(keluar[2]==0)&&(keluar[3]==0)&&(keluar[4]==0)&&

      (keluar[5]==0)&&(keluar[6]==0)&&(keluar[7]==0)&&(keluar[8]==0)&&(keluar[9]==1))

      cout<<"Keluaran = 9"<<endl;

   dapatkan();

}
