# Test-Informatika-14.03
Тест по информатика за 9 клас
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
void fill (int mas [][20], int n, int m)
{
    for (int i=0 ;i<n; i++)
        for(int j=0; j<m; j++)
        mas[i][j]=rand(); // cin>>mas[i][j];
}
void show (int mas [][20], int n, int m)
{
    for (int i=0; i<n; i++)
    {


        for (int j=0; j<m; j++)
        {
            cout<<mas[i][j]<<' ';}
        cout<<endl;
    }

}
void razguvane(int mas[][20],int n, int m)// razguvane po redove (samo za 1vi red)
{
    for (int i=0; i<1; i++)
        for (int j=0; j<m; j++){
    cout<<mas[i][j]<<' ';
}
}
void razguvane2(int mas[][20],int n, int m)// razguvane po koloni
{
    for (int i=0; i<2; i++)
        for (int j=0; j<n; j++)
        {
          cout<<mas[j][i]<<' ';// mas[j][i] !!!!!
        }
}
void razguvaneG (int mas[][20], int n, int m) // разгъване по буквата Г
{
    for (int i=0; i<1;i++)
        for (int j=0; j<m; j++)
        cout<<mas[i][j]<<' ';
    for (int i=0; i<n; i++)
        for (int j=0; j<1;j++)
        cout<<mas[i][j]<<' ';
}
int main ()
{
    int n,m,mas[20][20];
    cin>>n>>m;;
    fill(mas,n,m);
    show(mas,n,m);
    cout<<endl;
    razguvane(mas,n,m);
    cout<<endl;
    cout<<endl;
    razguvane2(mas,n,m);
    cout<<endl;
    razguvaneG(mas,n,m);
}

