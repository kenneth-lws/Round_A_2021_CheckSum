#include <iostream>
#include <string>
#include <stdlib.h>
#include<bits/stdc++.h>

using namespace std;

#define ll long long
#define ld long double

const int MxN = 1e3;
int t, r, c, n;
int A[501][501];
int B[501][501];
int64_t ans;

int p[MxN];
/*
int find(int x){
    if (x == p[x]){
        return x;
    }
    return p[x] = find(p[x]);
}

bool join(int x, int y){
    x = find(x);
    y = find(y);
    if (x == y){
        return false;
    }
    p[y] = x;
    return true;
}
*/

int solve(){
    cin >> n;
    ll answer = 0;
    vector<vector<int>> v;
    for(int i = 0; i < n; i++){
        for (int j = 0; j < n; j++){
            cin >> A[i][j];
        }
    }
    for(int i = 0; i < n; i++){
        for (int j = 0; j < n; j++){
            cin >> B[i][j];
            if (B[i][j] != 0){
                v.push_back({B[i][j],i,n+j});
            }
            answer += B[i][j];
        }
    }
    for (int i = 0; i < n; i++){
        cin >> r;
    } 
    for (int i = 0; i < n;i++){
        cin >> c;
    }
    sort(v.begin(),v.end());
    reverse(v.begin(),v.end());
    
    for (int i = 0; i < 2*n; i++){
        p[i] = i;
    }
    for (int i = 0; i < v.size(); i++){
        if (join(v[i][1], v[i][2])){
            answer -= v[i][0];
            //cout << answer << endl;
        }
    }
    return answer;
}

int main(){
    cin >> t ;
    for (int i = 0; i < t; i++){
        ans = solve();
        cout << "Case #" << i+1 <<": " << ans <<endl;
    }
    return 0;    
}
