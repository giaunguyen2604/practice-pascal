# Đề Tiền Giang năm 2012
## Link đề: Downloads/De%20nam%20HSG%202020_chinh%20thuc.pdf

### Bài 1

# Code

uses crt;
var s:string;
    f1,f2:text;
 
function chuyen(c:char):char;
var j:char;
    i,k,vt:byte;
    d:array[1..26] of char;
begin
vt:=0;
k:=0;
for j:='A' to 'Z' do
    begin
       inc(k);
       d[k]:=j;
    end;
for i:=1 to k do
if d[i]=c then
        begin
                vt:=i;
                break;
        end;
chuyen:=d[((26-vt) mod 26)+1];
end;
 
procedure nhap;
begin
assign(f1,'enco.inp'); reset(f1);
assign(f2,'enco.out'); rewrite(f2);
readln(f1,s);
end;
 
procedure xuat;
var i:integer;
begin
for i:=1 to length(s) do
if s[i] in ['A'..'Z'] then write(f2,chuyen(s[i])) else write(f2,s[i]);
end;
 
begin clrscr;
nhap;
xuat;
close(f1);
close(f2);
end.
Link: https://ideone.com/440fPE

# Bài 2:
# Code:
uses crt;
var n,i:int64;
f1,f2:text;
a:array[1..100000000] of int64;
begin clrscr;
assign(f1,'fibb.inp'); reset(f1);
assign(f2,'fibb.out'); rewrite(f2);
read(f1,n);
   repeat
      inc(i);
      read(f1,a[i]);
      if i>2 then
          if a[i]=a[i-1]+a[i-2] then continue
          else
                begin
                        writeln(f2,'NO');
                        close(f1);
                        close(f2);
                        exit;
                end;
   until i=n;
write(f2,'YES');
close(f1);
close(f2);
end.
Link: https://ideone.com/6ycaM9

# Bài 3:uses crt;
type mang=record
        ten:string;
        chieucao:real;
        donvi:string;
end;
var n,k:integer;
s:string;
f1,f2:text;
a:array[1..1000] of mang;
tmp:mang;
function ten(s:string):string;
var i:integer;
    x:string;
begin
x:='';
for i:=1 to length(s) do
if s[i] in ['A'..'z',' '] then x:=x+s[i] else break;
while x[length(x)]=' ' do delete(x,length(x),1);
ten:=x;
end;

function donvi(s:string):string;
var x:string;
    i:integer;
begin
x:='';
for i:=length(s) downto 1 do
if s[i] in ['A'..'z'] then x:=s[i]+x else break;
donvi:=x;
end;

function chieucao(s:string):real;
var i,code:integer;
        chcao:real;
        x:string;
begin
x:='';
for i:=1 to length(s) do
if s[i] in ['0'..'9','.'] then x:=x+s[i];
val(x,chcao,code);
chieucao:=chcao;
end;


procedure nhap;
var i:integer;
begin
assign(f1,'tall.inp'); reset(f1);
assign(f2,'tall.out'); rewrite(f2);
readln(f1,n,k);
for i:=1 to n do
        begin
                readln(f1,s);
                a[i].ten:=ten(s);
                a[i].chieucao:=chieucao(s);
                a[i].donvi:=donvi(s);
        end;
end;

procedure xuli;
var i,j:integer;
begin
for i:=1 to n do
        begin
                if a[i].donvi='m' then a[i].chieucao:=a[i].chieucao*1000;
                if a[i].donvi='dm' then a[i].chieucao:=a[i].chieucao*100;
                if a[i].donvi='cm' then a[i].chieucao:=a[i].chieucao*10;
        end;
for i:=1 to n-1 do
for j:=i+1 to n do
if a[i].chieucao<a[j].chieucao then
        begin
                tmp:=a[i];
                a[i]:=a[j];
                a[j]:=tmp;
        end;
end;

procedure xuat;
var i:integer;
begin
for i:=1 to k do
writeln(f2,a[i].ten);
end;

begin clrscr;
nhap;
xuli;
xuat;
close(f1);
close(f2);
end.
Link: https://ideone.com/Jjinf4

# Bài 4
# Đề: ![image](https://user-images.githubusercontent.com/79987495/110145727-51ae0b00-7e0c-11eb-90ff-a3f48567de47.png)
# Code:
uses crt;
var n,m,max,max2,kq:longint;
f1,f2:text;
a:array[1..10000,1..10000] of int64;

procedure nhap;
var i,j:integer;
begin
assign(f1,'multmax.inp'); reset(f1);
assign(f2,'multmax.out'); rewrite(f2);
readln(f1,n,m);
for i:=1 to n do
    begin
        for j:=1 to m do
        read(f1,a[i,j]);
    end;
end;

procedure xuli;
var i,j,hang:integer;
begin
kq:=0;
for i:=1 to n do
     begin
        max:=0;
        max2:=0;
        begin
           for j:=1 to m do
                        if a[i,j]>max then begin max:=a[i,j]; hang:=j; end;
           for j:=1 to m do
                        if (a[i,j]>max2) and (hang<>j) then max2:=a[i,j];

        if max*max2>kq then kq:=max*max2;
        end;
     end;
end;

begin clrscr;
nhap;
xuli;
writeln(f2,kq);
close(f1);
close(f2);
end.
https://ideone.com/cJwZN1

