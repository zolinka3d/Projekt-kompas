# Projekt-kompas
Środowisko : Windows Api
Biblioteki :
            #include <windows.h>
            #include <iostream>
            #include <vector>
            #include <fstream>
            #include <cmath>
            #include <stdio.h>
            #include <time.h> 
  zdefiniowane:
          #define idTimer 100
          #define time_stamp 100
          #define idTimer54 100
  zdefiniowane zmienne globalne:
          std::vector<double> roll, pitch, yaw;
          int ile2;
          double x = 1;
          double y = 3;
          MSG Komunikat;
          HWND hile;
          char ile[3];
   HWND h54Przycisk;
    HWND h11Przycisk;
    HWND h12Przycisk;
    HWND h22Przycisk;
    HWND h21Przycisk;     -   zdefiniowane przyciski
  użyte funckje:
  int convertToInt(); - konwertowanie zmiennej char na int
  void readRollAndPitchAndYaw();  - pobieranie danych z pliku
  double  calc_angle();   -   konwertowanie zmiennych pitch i roll w potrzebne do rysowania strzałki kompasu radiany
  LRESULT CALLBACK OkiennaProc(); - 
  int WINAPI WinMain();    -     odpowiedzialne za powstanie okna aplikacji,a na dole pętla komunikatów
                                    while( GetMessage( & Komunikat, NULL, 0, 0 ) )
                              {
                                  TranslateMessage( & Komunikat );
                                  DispatchMessage( & Komunikat );
                              }
                              return Komunikat.wParam;
   ShowWindow();   - pokazanie okna aplikacji
  CreateWindowEx();   -  tworzenie przycisków / tekstów statycznych lub adytowanych 
void rysowanie();   - zamazywanie wykresu
void rysowanie2();  - rysowanie wykresu
void rysowanie_wskazowki(); - rysowanie wskazówki kompasa
MoveToEx(); - początek rysowania lini
 LineTo(); - koniec rysowania linii
  void CALLBACK timer(); funckja odpowiedzialna za odmierzanie czasu, zawiera w środku rysowanie wykresów, żeby te mogły się rysować w czasie
  GetWindowText(); - wczytywanie charu z tekstu statycznego "hile"
  SetTimer(); - zaczęcie odliczania czasu
  KillTimer(); - koniec odliczania czasu
  SelectObject(); - zmiana koloru
  hdc = BeginPaint(hwnd,&ps); - rozpoczęscie rysowania
  
  Arc(); rysowanie elipsy / u mnie okręgu
  EndPaint(hwnd, &ps); - koniec rysowania
   DestroyWindow( hwnd ); - zamknięcie okna
  PostQuitMessage(); - w razie odpalonych komunikatów, kiedy zamkniemy program, mają się wyłączyć
  
  
  
  
  
  
