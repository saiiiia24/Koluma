# Koluma
program DO
real, dimension (100000) :: A, B, T, C, P, D, E, F !ввод исходных массивов
integer i, n, nt !переменные отвечающие за нумерацию величин

real St1, St2, St3, St4, St5, St6, St7, St8, St9, St10, St10, St11, St12, St13, St14, St15, St16, St17, St18 
!объявление переменной СУММА ТЕМПЕРАТУР

real Sp1, Sp2, Sp3, Sp4, Sp5, Sp6, Sp7, Sp8, Sp9, Sp10, Sp10, Sp11, Sp12, Sp13, Sp14, Sp15, Sp16, Sp17, Sp18
!объявление переменной СУММА ОСАДКОВ

real SRt1, SRt2, SRt3, SRt4, SRt5, SRt6, SRt7, SRt8, SRt9, SRt10, SRt10, SRt11, SRt12, SRt13, SRt14, SRt15, SRt16, SRt17, SRt18 
!объявление переменной СРЕДНЯЯ ТЕМПЕРАТУРА

real RP1, RP2, RP3, RP4, RP5, RP6, RP7, RP8, RP9, RP10, RP10, RP11, RP12, RP13, RP14, RP15, RP16, RP17, RP18 
!объявление переменной РЕЗУЛЬТАТ ВЫЧИСЛЕНИЯ ОСАДКОВ

i = 0     !обнуление переменных
St1 = 0
St2 = 0
St3 = 0
St4 = 0
St5 = 0
St6 = 0
St7 = 0
St8 = 0
St9 = 0
St10 = 0
St11 = 0
St12 = 0
St13 = 0
St14 = 0
St15 = 0
St16 = 0
St17 = 0
Sp1 = 0
Sp2 = 0
Sp3 = 0
Sp4 = 0
Sp5 = 0
Sp6 = 0
Sp7 = 0
Sp8 = 0
Sp9 = 0
Sp10 = 0
Sp11 = 0
Sp12 = 0
Sp13 = 0
Sp14 = 0
Sp15 = 0
Sp16 = 0
Sp17 = 0
SRt1 = 0 
SRt2 = 0
SRt3 = 0 
SRt4 = 0 
SRt5 = 0 
SRt6 = 0 
SRt7 = 0 
SRt8 = 0 
SRt9 = 0
SRt10 = 0
SRt11 = 0 
SRt12 = 0 
SRt13 = 0 
SRt14 = 0 
SRt15 = 0 
SRt16 = 0
SRt17 = 0
RP1 = 0
RP2 = 0
RP3 = 0
RP4 = 0
RP5 = 0
RP6 = 0
RP7 = 0
RP8 = 0
RP9 = 0
RP10 = 0
RP10 = 0
RP11 = 0
RP12 = 0
RP13 = 0
RP14 = 0
RP15 = 0
RP16 = 0
RP17 = 0
RP18 = 0


open (1, file = '....dat') !открытие файла данных
 do while (.not.eof(1))       
 i = i+1
 read (1,*) A(i), B(i), T(i), C(i), P(i), D(i), E(i), F(i)  !считывание информаци по столбцам
 i = n
 enddo
close(1)
write (*,*) n !вывод на экран количества величин в столбцах
stop

open (2, file = '....txt') !открытие файлов с результатами

!78 номер года
nt = 0 !обнуление переменной считающей ненулевые значения
do i = 1,1472
if (T(i).ne.0) then !отбор положительных переменных
St1 = St1 + T(i)     ! вычисление суммы температур
nt = nt + 1           !подсчет количества элементов в сумме
endif
SRt1 = St1/nt   !вычисление среднего 
enddo
write (2,*) SRt1 !запись результата в файл

!79
nt = 0
do i = 1473,4392
if (T(i).ne.0) then
St2 = St2 + T(i)
nt = nt + 1 
endif
SRt2 = St2/nt
enddo
write (2,*) SRt2

!80
nt = 0
do i = 4393,7320
if (T(i).ne.0) then
St3 = St3 + T(i)
nt = nt + 1 
endif
SRt3 = St3/nt
enddo
write (2,*) SRt3

!81
nt = 0
do i = 7321,10241
if (T(i).ne.0) then
St4 = St4 + T(i)
nt = nt + 1 
endif
SRt4 = St4/nt
enddo
write (2,*) SRt4

!82
nt = 0
do i = 10241,13160
if (T(i).ne.0) then
St5 = St5 + T(i)
nt = nt + 1 
endif
SRt5 = St5/nt
enddo
write (2,*) SRt5

!83
nt = 0
do i = 1361,16080
if (T(i).ne.0) then
St6 = St6 + T(i)
nt = nt + 1 
endif
SRt6 = St6/nt
enddo
write (2,*) SRt6

!84
nt = 0
do i = 16081,19008
if (T(i).ne.0) then
St7 = St7 + T(i)
nt = nt + 1 
endif
SRt7 = St7/nt
enddo
write (2,*) SRt7

!85
nt = 0
do i = 19009,21928
if (T(i).ne.0) then
St8 = St8 + T(i)
nt = nt + 1 
endif
SRt8 = St8/nt
enddo
write (2,*) SRt8

!86
nt = 0
do i = 21929,24848
if (T(i).ne.0) then
St9 = St9 + T(i)
nt = nt + 1 
endif
SRt9 = St9/nt
enddo
write (2,*) SRt9

!87
nt = 0
do i = 24849,27768
if (T(i).ne.0) then
St10 = St10 + T(i)
nt = nt + 1 
endif
SRt10 = St10/nt
enddo
write (2,*) SRt10

!88
nt = 0
do i = 27769,30696
if (T(i).ne.0) then
St11 = St11 + T(i)
nt = nt + 1 
endif
SRt11 = St11/nt
enddo
write (2,*) SRt11

!89
nt = 0
do i = 30697,33616
if (T(i).ne.0) then
St12 = St12 + T(i)
nt = nt + 1 
endif
SRt12 = St12/nt
enddo
write (2,*) SRt12

!90
nt = 0
do i = 33617,36536
if (T(i).ne.0) then
St13 = St13 + T(i)
nt = nt + 1 
endif
SRt13 = St13/nt
enddo
write (2,*) SRt13

!91
nt = 0
do i = 36541,39456
if (T(i).ne.0) then
St14 = St14 + T(i)
nt = nt + 1 
endif
SRt14 = St14/nt
enddo
write (2,*) SRt14

!92
nt = 0
do i = 39457,42384
if (T(i).ne.0) then
St15 = St15 + T(i)
nt = nt + 1 
endif
SRt15 = St15/nt
enddo
write (2,*) SRt15

!93
nt = 0
do i = 42385,45304
if (T(i).ne.0) then
St16 = St16 + T(i)
nt = nt + 1 
endif
SRt16 = St16/nt
enddo
write (2,*) SRt16

!94
nt = 0
do i = 45305,48224
if (T(i).ne.0) then
St17 = St17 + T(i)
nt = nt + 1 
endif
SRt17 = St17/nt
enddo
write (2,*) SRt17

!95
nt = 0
do i = 48225,51144
if (T(i).ne.0) then
St18 = St18 + T(i)
nt = nt + 1 
endif
SRt18 = St18/nt
enddo
write (2,*) SRt18


!78
do i = 1,1472
if (P(i).ne.0) then
Sp1 = Sp1 + P(i) !вычисление суммы осадков измеренных
endif
RP1 = Sp1*10800 !приведение к сумме годовых осадков
enddo
write (2,*) RP1

!79
do i = 1473,4392
if (P(i).ne.0) then
Sp2 = Sp2 + P(i)
endif
RP2 = Sp2*10800
enddo
write (2,*) RP2

!80
do i = 4393,7320
if (P(i).ne.0) then
Sp3 = Sp3 + P(i)
endif
RP3 = Sp3*10800
enddo
write (2,*) RP3

!81
do i = 7321,10241
if (P(i).ne.0) then
Sp4 = Sp4 + P(i)
endif
RP4 = Sp4*10800
enddo
write (2,*) RP4

!82
do i = 10241,13160
if (P(i).ne.0) then
Sp5 = Sp5 + P(i)
endif
RP5 = Sp5*10800
enddo
write (2,*) RP5

!83
do i = 13161,16080
if (P(i).ne.0) then
Sp6 = Sp6 + P(i)
endif
RP6 = Sp6*10800
enddo
write (2,*) RP6

!84
do i = 16081,19008
if (P(i).ne.0) then
Sp7 = Sp7 + P(i)
endif
RP7 = Sp7*10800
enddo
write (2,*) RP7

!85
do i = 19009,21928
if (P(i).ne.0) then
Sp8 = Sp8 + P(i)
endif
RP8 = Sp8*10800
enddo
write (2,*) RP8

!86
do i = 21929,24848
if (P(i).ne.0) then
Sp9 = Sp9 + P(i)
endif
RP9 = Sp9*10800
enddo
write (2,*) RP9

!87
do i = 24849,27768
if (P(i).ne.0) then
Sp10 = Sp10 + P(i)
endif
RP10 = Sp10*10800
enddo
write (2,*) RP10

!88
do i = 27769,30696
if (P(i).ne.0) then
Sp11 = Sp11 + P(i)
endif
RP11 = Sp11*10800
enddo
write (2,*) RP11

!89
do i = 30697,33616
if (P(i).ne.0) then
Sp12 = Sp12 + P(i)
endif
RP12 = Sp12*10800
enddo
write (2,*) RP12

!90
do i = 33617,36536
if (P(i).ne.0) then
Sp13 = Sp13 + P(i)
endif
RP13 = Sp13*10800
enddo
write (2,*) RP13

!91
do i = 36541,39456
if (P(i).ne.0) then
Sp14 = Sp14 + P(i)
endif
RP14 = Sp14*10800
enddo
write (2,*) RP14

!92d
do i = 39457,42384
if (P(i).ne.0) then
Sp15 = Sp15 + P(i)
endif
RP15 = Sp15*10800
enddo
write (2,*) RP15

!93
do i = 42385,45304
if (P(i).ne.0) then
Sp16 = Sp16 + P(i)
endif
RP16 = Sp16*10800
enddo
write (2,*) RP16

!94
do i = 45305,48224
if (P(i).ne.0) then
Sp17 = Sp17 + P(i)
endif
RP17 = Sp17*10800
enddo
write (2,*) RP17

!95
do i = 48225, 51144
if (P(i).ne.0) then
Sp18 = Sp18 + P(i)
endif
RP18 = Sp18*10800
enddo
write (2,*) RP18
end

end
