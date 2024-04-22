#include <iostream>
using namespace std;

void InMang(int a[], int N)
{
    for (int i = 0; i < N; i++)
        if (a[i] < 10)
            cout << a[i];
        else
        {
            cout << char('A' + a[i] - 10);
        }
}
void InCPhan(int a[], int N, int c, int p)
{
    if (p > N)
    {
        InMang(a, N);
        cout << endl;
    }
    else
    {
        for (int i = 0; i < c; i++){
            a[p-1] = i;
            InCPhan(a, N, c, p + 1);
        }
    }
}
