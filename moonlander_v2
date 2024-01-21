
5 rem Moonlander
10 cls
19 co=30:ro=5:gosub 5030:A1=1:A2=37:A3=40:GOSUB 5090
20 print "Moonlander";:GOSUB 5140:PRINT           
30 let t+0
30 let t=0
40 let h=500
50 let v=50
60 let f=150
65 co=18:ro=10:gosub 5030
70 print "Time     ";t,"Height ";h  
75 co=18:ro=12:gosub 5030 
80 print "Velocity ";v,"Fuel   ";f
90 if F=0 then goto 140
95 co=30:ro=18:gosub 5030
100 print "Burn? (0-30)"
105 co=30:ro=19:gosub 5030
110 input b
120 if b<0 then let b=0
130 if b>30 then let b=30
140 if b>f then let b=f
150 let v1=v-b+5
160 let f=f-b
170 if (v1+v)/2>=h then goto 220
180 let h=h-(v1+v)/2
190 let t=t+1
200 let v=v1
210 goto 65
220 let v1=v+(5-b)*h/v
225 co=25:ro=25:gosub 5030
226 A1=5:A2=37:A3=40:GOSUB 5090                                 
230 if v1>5 then print "you crashed - all dead!";
240 if v1>1 and v1<=5 then print "ok - but some injuries";
250 if v1<=1 then print "good landing!";
255 GOSUB 5140:PRINT
260 stop

5020 REM Set cursor pos ro=row, co=col
5030 RO$=STR$(RO):RO$=RIGHT$(RO$,LEN(RO$)-1)
5040 CO$=STR$(CO):CO$=RIGHT$(CO$,LEN(CO$)-1)
5050 PRINT CHR$(27)+"["+RO$+";"+CO$+"H";
5070 RETURN

5080 REM SET ATTRIBUTES A1=attribute, A2=Foreground color, A3=Background color
5090 A1$=STR$(A1):A1$=RIGHT$(A1$,LEN(A1$)-1)
5100 A2$=STR$(A2):A2$=RIGHT$(A2$,LEN(A2$)-1)
5110 A3$=STR$(A3):A3$=RIGHT$(A3$,LEN(A3$)-1)
5120 PRINT CHR$(27)+"["+A1$+";"+A2$+";"+A3$+"m";:RETURN

5130 REM RESET ATTRIBUTES
5140 PRINT CHR$(27)+"[0m";:RETURN
