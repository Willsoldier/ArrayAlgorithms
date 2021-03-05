//Challenging assignment from my C++ course at my local college
#include <iostream>
using namespace std;

//Function Prototypes
int main(void);
int getSIWSmallestTODCWilliamG(int* arrayWG, int sizeWG);
void displayClassInfoWilliamG(void);

//Application Driver
int main() {
    int inputWG = 0;
    int sizeWG = 0;
    int* arrayWG;
    int tempWG = 0;
    int tudWG = 0;
    int smallestIntWG;
    int smallestTudWG = 0;
    int tinyTudWG = 10;


    displayClassInfoWilliamG();
    do {
        cout << "\n*******************************************\n"
            "*              MENU - HW #2               *\n"
            "*  (1) Calling getSIWSmallestTODCWilliamG *\n"
            "*  (2) Quit                               *\n"
            "*******************************************\n";
        cin >> inputWG;
        cout << "\n";
        switch (inputWG) {
        case 1:
        {
            cout << "What is the size of the array?: ";
            cin >> sizeWG;

            arrayWG = new int[sizeWG];

            for (int i = 0; i < sizeWG; i++) {
                cout << "   Value #" << i + 1 << ": ";
                cin >> arrayWG[i];
            }

            cout << "The working array has " << sizeWG << " values of\n";
            for (int i = 0; i < sizeWG; i++) {
                cout << "   Value " << i + 1 << ": " << arrayWG[i] << "\n";
            }
            cout << endl;

            cout << "Calling getSIWSmallestTODCWilliamG() with argument of\n"
                "   The array { ";
            for (int i = 0; i < sizeWG; i++) {
                cout << arrayWG[i] << " ";
            }
            cout << "}; and\n   The array size of " << sizeWG << "\n";

            cout << "\n  For individual values -\n";
            for (int i = 0; i < sizeWG; i++) {
                int tempArray[10]{ 0 };
                arrayWG[i] > 0 ? tempWG = arrayWG[i] : tempWG = -arrayWG[i];

                while (tempWG > 0) {
                    ++tempArray[tempWG % 10];
                    tempWG /= 10;
                }
                tempWG = 0;


                for (int i = 0; i < 10; ++i) {
                    if (tempArray[i] != 0) {
                        ++tudWG;
                    }
                }
                if (tinyTudWG > tudWG) {
                    tinyTudWG = tudWG;
                }
                cout << "  " << arrayWG[i] << " has " << tudWG << " unqiue digit(s).\n";
                tudWG = 0;
            }

            smallestIntWG = getSIWSmallestTODCWilliamG(arrayWG, sizeWG);

            int tempArray2[10]{ 0 };
            smallestIntWG > 0 ? tempWG = smallestIntWG : tempWG = -smallestIntWG;
            
            while (tempWG > 0) {
                ++tempArray2[tempWG % 10];
                tempWG /= 10;
            }
            tempWG = 0;

            for (int i = 0; i < 10; ++i) {
                if (tempArray2[i] != 0) {
                    ++smallestTudWG;
                }
            }
            cout << "\n\nAfter the function call was completed and a value was returned\n\n"
                "  (1) The smallest TUD is " << tinyTudWG << " and;\n"
                "  (2) " << smallestIntWG << " is the smallest integer with a smallest TUD of " << smallestTudWG;

            cout << "\n";
            delete[] arrayWG;
        }
        case 2:
            break;
        default:
            "Wrong option, try again";
            break;
        }
    } while (inputWG != 2);
    return 0;
}

//Function Definition
int getSIWSmallestTODCWilliamG(int* arrayWG, int sizeWG) {
    int smallestIntWG = arrayWG[0];
    int tudWG = 0;
    int remWG = 0;
    int smallestTUD = 0;
    int tempWG = 0;


    //Find smallest integer in array
    for (int i = 0; i < sizeWG; i++) {
        if (arrayWG[i] < smallestIntWG) {
            smallestIntWG = arrayWG[i];
        }
    }

    return smallestIntWG;

}

//Function Definition
void displayClassInfoWilliamG() {
    cout << "CIS 25 - C++ Programming\n"
        "TEST";
}
