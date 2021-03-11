## Bài 1
```
n:int64; 
function kt(n:int64):boolean; 
var s:string; k,i,code:integer; 
begin str(n,s); 
for i:=1 to length(s) do 
if s[i]<>'0' then 
begin 
val(s[i],k,code); 
if n mod k<>0 then exit(false); 
end; exit(true); 
end; 
begin 
readln(n); 
n:=n-1; 
repeat; 
inc(n); 
until kt(n); 
write(n);  
end.
```

## Bài 2
```
s:string; 
function kt1(s:string):boolean; 
var d,i:integer; 
begin d:=1; 
for i:=1 to length(s) do 
begin 
if chr(ord(s[i])+1)=s[i+1] then inc(d); 
if d>=4 then exit(true); 
if chr(ord(s[i])+1)<>s[i+1] then d:=1; 
end; exit(false); end; 
function kt2(s:string):boolean; 
var d,i:integer; 
begin d:=1; 
for i:=1 to length(s)-1 do 
begin 
if s[i]=s[i+1] then inc(d); 
if d>=3 then exit(true); 
if s[i]<>s[i+1] then d:=1; end; exit(false); 
end; 
function kt3(s:string):boolean; 
var d,i:integer; 
begin d:=0; 
for i:=1 to length(s)-1 do 
if s[i]=s[i+1] then 
begin d:=i; break; 
end; 
if (d=0) or (d>=9) then exit(false); 
for i:=d to length(s)-1 do if s[i]=s[i+1] then exit(true); 
exit(false); end; 
function kt4(s:string):boolean; 
var d,i,j:integer; 
begin 
for i:=1 to length(s)-5 do 
begin d:=1; for j:=i+1 to length(s) do 
if s[j]=s[i] then inc(d); if d>=5 then exit(true); 
end; exit(false); 
END; 
begin 
readln(s); 
if (kt1(s)) or(kt2(s)) or(kt3(s)) or(kt4(s)) then begin write(f2,'YES'); exit; end; 
write('NO');  end.
```
## Bài 3
```
var f1,f2:text; a,b,c,d,t,i:integer; 
function kt(n:integer):integer; 
begin if n>12 then n:=n-12; kt:=n; end; 
begin 
read(f1,a,b,c,d); 
b:=b div 5; d:=d div 5; 
if b=0 then inc(t,kt(a)); 
if (b<=6) then inc(t); 
if d>0 then inc(t,kt(c)); 
if (d>=6) then inc(t); 
if c-a>=2 then begin 
for i:=a+1 to c-1 do 
t:=t+kt(i)+1; end; write(f2,t); 
end.
```
## Bài 4
```
s:string; 
n,i,j,k,d,h:integer; x:string; 
begin 
readln(f1,s); readln(f1,n); 
for i:=1 to n do begin 
d:=0; 
readln(f1,x); 
for j:=1 to length(s) do 
begin 
  for k:=1 to length(x) do 
  if x[k]=s[j] then inc(d); 
end; if d=length(x) then inc(h); 
end; 
write(f2,h); 
end.
```

© 2021 GitHub, Inc.
