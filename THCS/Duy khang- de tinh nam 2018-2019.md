## Hinh anh:
![159958407_2841514022828918_4530642650663186876_n](https://user-images.githubusercontent.com/80033114/111069928-f2ce4d00-8501-11eb-8404-f1cb0f5cfe56.jpg)
![159094245_556917745276740_5913544727239947830_n](https://user-images.githubusercontent.com/80033114/111069931-f4981080-8501-11eb-981d-80abb795164c.jpg)
![159628180_177963980620756_2514788797229231977_n](https://user-images.githubusercontent.com/80033114/111069936-f661d400-8501-11eb-952f-2737a0fa351f.jpg)
![159653664_233983128411803_6712054165517256296_n](https://user-images.githubusercontent.com/80033114/111069924-ef3ac600-8501-11eb-882f-c2a0f95d047e.jpg)
# Bai 1
```
uses crt;
type mang=record
        gbd,pbd,gkt,pkt:integer;
{gbd:gio bat dau; pbd:phutbatdau; gkt:gio ket thuc; phut ket thuc}
end;
var n,h,code,tong2,min1,min2,max1,max2,i,l,j:integer;
    s,x:string;
    a:array[1..100] of mang;
    tmp:mang;
function dinhdang(n:integer):string;
var s:string;
begin
        str(n,s);
        if n<10 then s:='0'+s;
        kt:=s;
end;
procedure nhap;
begin
readln(n);
for i:=1 to n do
begin
        readln(s);
        for j:=1 to length(s) do
        if s[j] in ['0'..'9'] then begin l:=j; break; end;
        x:=copy(s,l,2);
        val(x,h,code); a[i].gbd:=h;
        x:=copy(s,l+3,2);
        val(x,h,code); a[i].pbd:=h;
        x:=copy(s,l+6,2);
        val(x,h,code); a[i].gkt:=h;
        x:=copy(s,l+9,2);
        val(x,h,code); a[i].pkt:=h;
end;
end;
procedure xuli;
begin
tong1:=0;
tong2:=0;
for i:=1 to n-1 do
for j:=i+1 to n do
    if (a[i].gbd>a[j].gkt) or ((a[i].gbd=a[j].gkt) and (a[i].pbd>a[j].pkt)) then
        begin
                tmp:=a[i];
                a[i]:=a[j];
                a[j]:=tmp;
        end;
min1:=a[1].gbd; min2:=a[1].pbd; max1:=a[1].gkt; max2:=a[1].pkt;
tong1:=tong1+60-a[1].pbd+a[1].pkt+(a[1].gkt-a[1].gbd-1)*60;
for i:=2 to n do
begin
if a[i].gbd<=min1 then
        if a[i].pbd<min2 then begin min1:=a[i].gbd; min2:=a[i].pbd; end;
if a[i].gkt>=max1 then
        if a[i].pkt>max2 then begin max1:=a[i].gkt; max2:=a[i].pkt; end;
tong1:=tong1+60-a[i].pbd+a[i].pkt+(a[i].gkt-a[i].gbd-1)*60;
tong2:=tong2+60-a[i-1].pkt+a[i].pbd+(a[i].gbd-a[i-1].gkt-1)*60;
end;
        writeln(kt(min1),':',kt(min2));
        writeln(kt(max1),':',kt(max2));
        writeln(kt(tong1 div 60),':',kt(tong1 mod 60));
        writeln(kt(tong2 div 60),':',kt(tong2 mod 60));
end;

begin
nhap;
xuli;
end.
```

### **Nhận xét**

```diff
-  Thay đổi phương pháp xử lý trên số thực sẽ tốt hơn.
```


# Bai 2
```
uses crt;
var n:qword;
function kt(n:qword):boolean;
var s:string; i:integer;
begin
        str(n,s);
for i:=1 to length(s)-1 do
        if s[i]=s[i+1] then exit(false);
exit(true);
end;
procedure nhap;
begin
        read(n);
end;
procedure xuli;
begin
repeat;
        inc(n);
until kt(n);
write(n);
end;
begin
        nhap;
        xuli;
end.
```

### **Nhận xét**

```diff
-  Tạm ổn
-  Duyệt như này chỉ phù hợp đối với test nhỏ
```

# Bai 3
```
uses crt;
var a:array[1..2000] of integer;
k,n,i:integer;
procedure nhap;
begin
readln(k);
readln(n);   
if k-n<>1 then write('NO') else writeln('YES');
for i:=1 to n do
begin
        read(a[i]);
end;
end;
procedure xuli;
begin
for i:=1 to n-1 do
if a[i]+1<>a[i+1] then write(a[i]+1,' ');
end;
begin
        nhap;
        if k-1=n then xuli;
end.
```

### **Nhận xét**

```diff
- Lưu ý: chỉ in ra 1 số --> cần thiết dùng lệnh break để end for loop
- Code còn trên 1 
```

# Bai 4
```
var  x,s,maxln,maxnt,h:string;
n,m,i:longint;
function ktnt(s:string):boolean;
var n,i,code:longint;
begin
        val(s,n,code);
        if n<2 then exit(false);
for i:=2 to trunc(sqrt(n)) do
        if n mod i=0 then exit(false);
exit(true);
end;
procedure nhap;             {maxln:so lon nhat; maxnt:so nguyento lon nhat}
begin
  readln(n,m);
  str(n,s); str(m,x);
  if s>x then maxln:=s else maxln:=x;
end;
procedure xuli;
begin h:=x; maxnt:='0';
for i:=1 to length(s) do
begin
        x:=h;
        x[1]:=s[i];
if (ktnt(x)) and(x>maxnt) then maxnt:=x;
if x>maxln then maxln:=x;
        x:=h;
        x[length(x)]:=s[i];
if (ktnt(x)) and(x>maxnt) then maxln:=x;
if x>maxln then maxln:=x;
end;
if maxnt='0' then writeln(maxln) else writeln(maxnt);
end;
begin
        nhap;
        xuli;
end.
```

# Bai 5

```
var i,j,b:longword;
procedure nhap;
begin
readln(b);
end;
procedure xuli;
begin
writeln(b,' ',b);
for i:=1 to b*b do
if i<>b then
begin
        for j:=i+1 to b*b do
        if b=(2*i*j)/(i+j) then
        begin
                writeln(i,' ',j);
                writeln(j,' ',i);
                break;
        end;
end;
end;
begin
        nhap;
        xuli;
end.
```


### **Nhận xét**

```diff
- Điều quan trọng ở bài này là dùng kiến thức toán học hoặc phép thử trên vài bộ số (a, b, c) để giới hạn được phạm vi của a, c 
```

- [x]
