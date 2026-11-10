EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION

clc;

clear;

x = [1 1 1 1];

h = [1 2 3 4];

m = length(x);

n = length(h);

a=0:1:m-1;

b=0:1:n-1;

subplot(3,1,1);

plot2d3(a,x);

xlabel('Time');

ylabel('Amplitude');

title('Graphical Representation of Input Signal X');

subplot(3,1,2);

plot2d3(b,h);

xlabel('Time');

ylabel('Amplitude');

title('Graphical Representation of Impulse Signal h');

for i = 1: n+m-1

conv_sum = 0;

for j = 1:i

if (((i-j+1) <= n)&(j <=m))

conv_sum = conv_sum + x(j)*h(i-j+1);

end;

y(i) = conv_sum;

end;

end;

disp(y,'Convolution Sum using Direct Formula Method = ')

subplot(3,1,3);

plot2d3(y)

title('Graphical Representation of output Signal y');




### CALCULATIONS:
<img width="779" height="1308" alt="image" src="https://github.com/user-attachments/assets/08df290f-6fe9-4886-ae81-fa9d067d509e" />

<img width="900" height="1344" alt="image" src="https://github.com/user-attachments/assets/af7c7662-7cc0-40d1-91b5-451b186623f7" />

<img width="900" height="1360" alt="image" src="https://github.com/user-attachments/assets/747ad905-0808-402a-ad9b-40b8d9528184" />


### SAMPLE OUTPUT:

<img width="822" height="810" alt="image" src="https://github.com/user-attachments/assets/11151dd0-c005-4adf-a316-ef3ecff5004d" />




RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
