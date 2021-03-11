# DE THI HUYEN 
# link: 
KHONG BIET GUI ANH
## BAI 1

```
var f1,f2:text;
n:int64;
function kt(n:int64):boolean;
var s:string;  k,i,code:integer;
begin
str(n,s);
for i:=1 to length(s) do
if s[i]<>'0' then
begin
val(s[i],k,code);
if n mod k<>0 then exit(false);
end;
exit(true);
end;
begin
assign(f1,'NUM.INP'); reset(f1);
assign(f2,'NUM.OUT'); rewrite(f2);
readln(f1,n);
n:=n-1;
repeat;
inc(n);
until kt(n);
write(f2,n);
close(f1);
close(f2);
end.
```

## BAI 2

```
var f1,f2:text;
s:string;
function kt1(s:string):boolean;
var d,i:integer;
begin
d:=1;
for i:=1 to length(s) do
begin
        if chr(ord(s[i])+1)=s[i+1] then inc(d);
        if d>=4 then exit(true);
        if chr(ord(s[i])+1)<>s[i+1] then d:=1;
end;
exit(false);
end;
function kt2(s:string):boolean;
var d,i:integer;
begin
d:=1;
for i:=1 to length(s)-1 do
begin
        if s[i]=s[i+1] then inc(d);
        if d>=3 then exit(true);
        if s[i]<>s[i+1] then d:=1;
end;
exit(false);
end;
function kt3(s:string):boolean;
var d,i:integer;
begin
d:=0;
for i:=1 to length(s)-1 do
        if s[i]=s[i+1] then begin d:=i; break; end;
if (d=0) or (d>=9) then exit(false);
for i:=d to length(s)-1 do
        if s[i]=s[i+1] then exit(true);
exit(false);
end;
function kt4(s:string):boolean;
var d,i,j:integer;
begin
for i:=1 to length(s)-5 do
begin
d:=1;
for j:=i+1 to length(s) do
if s[j]=s[i] then inc(d);
if d>=5 then exit(true);
end;
exit(false);
END;
begin
assign(f1,'PHONE.INP'); reset(f1);
assign(f2,'PHONE.OUT'); rewrite(f2);
readln(f1,s);
if (kt1(s)) or(kt2(s)) or(kt3(s)) or(kt4(s)) then begin write(f2,'YES'); close(f1); close(f2); exit; end;
write(f2,'NO');
close(f1); close(f2);
end.
```

## BAI 3

```
var f1,f2:text;
a,b,c,d,t,i:integer;
function kt(n:integer):integer;
begin
if n>12 then n:=n-12;
kt:=n;
end;
begin
assign(f1,'CLOCK.INP'); reset(f1);
assign(f2,'CLOCK.OUT'); rewrite(f2);
read(f1,a,b,c,d);
b:=b div 5;
d:=d div 5;
if b=0 then inc(t,kt(a));
if (b<=6) then inc(t);
if d>0 then inc(t,kt(c));
if (d>=6)  then inc(t);
if c-a>=2 then begin
for i:=a+1 to c-1 do
t:=t+kt(i)+1;
end;
write(f2,t);
close(f1);
close(f2);
end.
```

## BAI 4

```
var f1,f2:text;
s:string;
n,i,j,k,d,h:integer;
x:string;
begin
assign(f1,'CIPHER.INP'); reset(f1);
assign(f2,'CIPHER.OUT'); rewrite(f2);
readln(f1,s);
readln(f1,n);
for i:=1 to n do
begin
d:=0;
readln(f1,x);
for j:=1 to length(s) do
begin
for k:=1 to length(x) do
if x[k]=s[j] then inc(d);
end;
if d=length(x) then inc(h);
end;
write(f2,h);
close(f1);
close(f2);
end.
```

