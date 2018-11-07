clear
format long;
N=200;
l=9.8e-2;
A=1.3*17.7*1e-4;
f=50;

Idata=[5.3 9.7 16.3 21.2 25.4 29.4 34 38.2 43.2 48.7 54.5 48.5 42.9 37.9 33.2 28.8 24.5 20.2 15.6 9.31 5.14 ]
Vdata=[162e-3 364e-3 826e-3 1.33 1.86 2.41 2.95 3.51 4.03 4.58 5.13 4.58 4.04 3.49 2.94 2.41 1.87 1.35 0.857 0.394 0.184]

Hdata=N.*Idata/(l);
Bdata=Vdata./(2*pi*f*N*A)
H=Hdata*1e-3;
B=Bdata;
len=length(B);
Bmax=B(len);
a=polyfit(B,H,5)
for n=1:101;
   Bfit(n)=Bmax*(n-1)/100; Hiron(n)=a(1)*Bfit(n)^5+a(2)*Bfit(n)^4+a(3)*Bfit(n)^3+a(4)*Bfit(n)^2+a(5)*Bfit(n)+a(6);   
end
plot (Hdata,Bdata);grid;
hold 
plot (Hiron,Bfit)
hold
xlabel('H [A turns]')
ylabel('B [T]')
