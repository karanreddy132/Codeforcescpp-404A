# Codeforcescpp-404A
#include <bits/stdc++.h>

using namespace std;

int main()
{
  int n;
  string s[301];
  cin >> n;
  for(int i=0;i<n;i++){
    cin >> s[i];
  }
  for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
      if(((i==j || i+j==n-1) && s[i][j]!=s[0][0]) || (s[0][0]==s[0][1]) || (i!=j && i+j!=n-1 && s[i][j]!=s[0][1])){
        cout << "NO";
        return 0;
      }
    }
  }
  cout << "YES";
  return 0;
}
