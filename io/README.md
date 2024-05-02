# Beispielprogramm zum Lesen von Wörtern aus einer Datei

`
#include<iostream>
#include<fstream>

using namespace std;

int main(int argc, char* argv[]) {
     if(argc < 2) {
         cout << "Dateiname muss als Argument angegeben werden!";
         return 1;
     }

    ifstream inputFile((string)argv[1]);

    string word;
    while(!inputFile.eof() && inputFile >> word) {
        cout << word << endl;
    }

    return 0;   
}
`
