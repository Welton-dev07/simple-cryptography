#include <iostream>
using namespace std;

int main() {
    string texto;
    cout << "Digite um texto: ";
    getline(cin, texto);

    string criptografado = "";

    for (int i = 0; i < texto.length(); i++) {
        criptografado += char(texto[i] + 3);
    }

    cout << "Texto criptografado: " << criptografado;

    char opcao;
    cout << "\nDeseja descriptografar? (S/N): ";
    cin >> opcao;

    if (opcao == 'S' || opcao == 's') {
        string original = "";
        for (int i = 0; i < criptografado.length(); i++) {
            original += char(criptografado[i] - 3);
        }
        cout << "Texto original: " << original;
    }

    return 0;
}
