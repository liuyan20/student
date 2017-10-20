//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;
//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------

void __fastcall TForm1::FormCreate(TObject *Sender)
{
 Timer1->Enabled=False;
   Memo1->Clear();
   Memo2->Clear();
   Edit1->Text="2";
   Edit2->Text="0";
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button1Click(TObject *Sender)
{
if(OpenDialog1->Execute());
   Memo1->Lines->LoadFromFile(OpenDialog1->FileName);   
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button2Click(TObject *Sender)
{
 Close();        
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button3Click(TObject *Sender)
{
 if(Memo1->Lines->Count)
      Timer1->Enabled=True;
   else
      ShowMessage("请导入名单");
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Timer1Timer(TObject *Sender)
{
Edit2->Text=rand();        
}
//---------------------------------------------------------------------------
void __fastcall TForm1::Button4Click(TObject *Sender)
{
   if(Timer1->Enabled)
    {
    Memo2->Clear();
    int a;
    int b;
    int m;
    int n;
    b=StrToInt(Edit1->Text);
    for(m=0;m<b;m++)
    {
        a=Memo1->Lines->Count;
        Memo2->Lines->Add(Memo1->Lines->Strings[rand()%a]);
        for(n=0;n<a;n++)
        {
          if(Memo1->Lines->Strings[n]==Memo2->Lines->Strings[m])
            {
             Memo1->Lines->Delete(n);
            }
        }
     }
     }
     if(Timer1->Enabled==false)
       ShowMessage("请先点击开始");
     Timer1->Enabled=False;
}
//---------------------------------------------------------------------------
