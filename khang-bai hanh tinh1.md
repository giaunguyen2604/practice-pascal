program ideone;
begin
	(* uses crt;
var batdau,ketthuc,ngay1,ngay2:string;
d,code,k,i,ngay3,ngay4:integer;
procedure nhap;
begin
readln(batdau);
readln(ketthuc);
for i:=1 to length(batdau) do
if batdau[i] in ['A'..'z'] then begin k:=i; break; end;
ngay1:=copy(batdau,1,pos(' ',batdau)-1);
val(ngay1,ngay3,code);
ngay2:=copy(ketthuc,1,pos(' ',ketthuc)-1);
val(ngay2,ngay4,code);
delete(batdau,1,k-1);
if batdau='Monday' then d:=1 else
if batdau='Tuesday' then d:=2 else
if batdau='Wednesday' then d:=3 else
if batdau='Thursday' then d:=4 else
d:=5;
d:=d+abs(ngay4-ngay3);
if d>5 then d:=d-5;
if d=1 then write('Monday') else
if d=2 then write('Tuesday') else
if d=3 then write('Wednesday') else
if d=4 then write('Thursday') else
write('Friday');
end;
begin
nhap;
readln;
end.


your code goes here *)
end.
