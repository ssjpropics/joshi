# joshi
entno()
{
count=0
num=${arr[$i]}
while [ $num -ne 0 ]
do
num=`expr $num / 10`
count=`expr $count + 1`
done
if [ $count -eq 3 ]
then
h=1
echo $h
else
k=0
echo $k
fi
}

fnrpocc()
{
arr[0]=$1
arr[1]=$2
arr[2]=$3
arr[3]=$4
arr[4]=$5
arr[5]=$6
i=0
while [ $i -lt 6 ]
do
x=`entno ${arr[$i]}`
if [ $x -eq 0 ]
then
echo ONE OF THE PARAMETERS IS NOT A 3 DIGIT NUMBER
exit
fi
ar2[$i]=$x
i=`expr $i + 1`
done
echo NUMBERS ARE
echo ${arr[@]}
tmp=0
i1=0
while [ $i1 -lt 6 ]
do
i2=`expr $i1 + 1`
cnt=0
while [ $i2 -lt 6 ]
do
if [ ${arr[$i1]} -eq ${arr[$i2]} ]
then
cnt=`expr $cnt + 1`
fi
i2=`expr $i2 + 1`
done
if [ $tmp -lt $cnt ]
then
tmp=`expr $cnt + 1`
tmpv=$i1
fi
ccnt[$i1]=$cnt
i1=`expr $i1 + 1`
done
if [ $tmp -eq 0 ]
then
echo NO NUMBER IS REPEATED
else
echo THE MAXIMUM OCCURED NUMBER ${arr[$tmpv]} HAS OCCURED $tmp TIMES
fi
}














***   next ***



. countno.sh
echo ENTER 6 three digits number
read a
read b
read c
read d
read e
read f
fnrpocc $a $b $c $d $e $f
