// KAHVE OTOMASYON SİSTEMİ

#include <stdio.h>
#include <conio.h>
#include <stdlib.h>

int main()
{
    int tutar;
    int toplamtutar = 0;
    int odenen = 0;
    int ekodeme = 0;
    int geriodeme = 0;
    int adet = 0;

    char secim;
    do {

        do {
            int yataycerceve = 50;
            int dikeycerceve = 15;
            system("Color F1");
            printf("\n\n\n\n\t\t\t");
            printf("%c", 201);
            for (int i = 0; i < yataycerceve; i++) printf("%c", 205);
            printf("%c", 187);
            printf("\n\t\t\t");
            for (int p = 0; p < dikeycerceve; p++) {

                printf("%c", 186);

                int j = 0;
                do {
                    if (j == 12 && p == 3)
                    {
                        printf("SANAL KAFEYE HOSGELDINIZ");
                        yataycerceve = yataycerceve - 23;
                    }
                    else if (j == 8 && p == 7)
                    {
                        printf("Devam etmek icin D veya d tusuna basiniz");
                        yataycerceve = yataycerceve - 39;
                    }
                    else if (j == 10 && p == 8)
                    {
                        printf("CIKIS icin ESC tusuna basiniz");
                        yataycerceve = yataycerceve - 28;
                    }
                    else
                    {
                        printf(" ");
                    }
                    j++;
                } while (j < yataycerceve);

                yataycerceve = 50;

                printf("%c", 186);
                printf("\n\t\t\t");
            }

            printf("%c", 200);
            for (int i = 0; i < yataycerceve; i++) printf("%c", 205);
            printf("%c", 188);
            printf("\n\n\n\n");

            secim = _getch();

            if (secim == 'D' || secim == 'd')
            {

                system("CLS");
                printf("\n\n\n\n\n\t\t\t\t\t");
                printf("KAHVE CESITLERI\n");
                printf("\t\t\t\t");
                printf("---------------------------------------\n");
                printf("\n\n\t\t\t\t");
                printf("1- TURK KAHVESI \t 40 TL\n");
                printf("\n\t\t\t\t");
                printf("2- ESPRESSO \t\t 33 TL\n");
                printf("\n\t\t\t\t");
                printf("3- MOCHA \t\t 70 TL \n");
                printf("\n\t\t\t\t");
                printf("4- AMERICANO \t\t 47 TL\n");
                printf("\n\t\t\t\t");
                printf("5- CAPPUCINO \t\t 52 TL \n");
                printf("\n\t\t\t\t");
                printf("6- CAFFE LATTE \t\t 54 TL \n");
                printf("\n\t\t\t\t");
                printf("7- SICAK CIKOLATA \t 69 TL\n");
                printf("\n\t\t\t\t");
                printf("8- SALEP \t\t 73 TL \n");

                printf("\n\n\n\t\t\t\t");
                printf("Lutfen seciminizi yapiniz: ");

                secim = _getch();
                system("CLS");
                system("Color E0");
                switch (secim)
                {
                case '1': {

                    system("CLS");
                    system("Color E0");
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("TURK KAHVESI MENUSU \n");
                    printf("\t\t\t\t");
                    printf("---------------------------------------\n");
                    printf("\n\n\t\t\t\t");
                    printf("1- SUTLU TURK KAHVESI \t\t  49TL\n");
                    printf("\n\t\t\t\t");
                    printf("2- DAMLA SAKIZLI TURK KAHVESI \t  46TL\n");
                    printf("\n\t\t\t\t");
                    printf("3- CIKOLATALI TURK KAHVESI \t  50 TL\n");
                    printf("\n\t\t\t\t");
                    printf("4- SADE TURK KAHVESI \t\t  40 TL\n");
                    printf("\n\n\n\t\t\t\t");
                    printf("Lutfen seciminizi yapiniz: ");

                    secim = _getch();

                    switch (secim)
                    {
                    case '1': {

                        system("CLS");
                        tutar = 49;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet SUTLU TURK KAHVESI istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet SUTLU TURK KAHVESI  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;

                    case '2': {

                        system("CLS");
                        tutar = 46;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet DAMLA SAKIZLI TURK KAHVESI istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet DAMLA SAKIZLI TURK KAHVESI  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;

                    case '3': {

                        system("CLS");
                        tutar = 50;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet CIKOLATALI TURK KAHVESI istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet CIKOLATALI TURK KAHVESI  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;

                    case '4': {

                        system("CLS");
                        tutar = 40;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet SADE TURK KAHVESI istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet SADE TURK KAHVESI  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;

                    default: {
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                    }
                    }

                } break;
                case '2': {

                    system("CLS");
                    system("Color E0");
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("ESPRESSO MENU\n");
                    printf("\t\t\t\t");
                    printf("---------------------------------------\n");
                    printf("\n\n\t\t\t\t");
                    printf("1- DOUBLE ESPRESSO  \t\t  43TL\n");
                    printf("\n\t\t\t\t");
                    printf("2- ESPRESSO MACCHIATO  \t\t  40TL\n");
                    printf("\n\t\t\t\t");
                    printf("3- DOUBLE ESPRESSO MACCHIATO  \t  46TL \n");
                    printf("\n\t\t\t\t");
                    printf("4- ESPRESSO  \t\t\t  33TL \n");
                    printf("\n\n\n\t\t\t\t");
                    printf("Lutfen seciminizi yapiniz: ");

                    secim = _getch();
                    switch (secim)
                    {
                    case '1': {

                        system("CLS");
                        tutar = 43;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet DOUBLE ESPRESSO istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet DOUBLE ESPRESSO icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;
                    case '2': {

                        system("CLS");
                        tutar = 40;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet ESPRESSO MACCHIATO istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet ESPRESSO MACCHIATO icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;
                    case '3': {

                        system("CLS");
                        tutar = 46;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet DOUBLE ESPRESSO MACCHIATO  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet DOUBLE ESPRESSO MACCHIATO  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;
                    case '4': {

                        system("CLS");
                        tutar = 33;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet ESPRESSO  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet ESPRESSO  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    }break;
                    default: {
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                    }
                    }

                } break;
                case '3': {

                    system("CLS");
                    system("Color E0");
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("MOCHA MENU\n");
                    printf("\t\t\t\t");
                    printf("---------------------------------------\n");
                    printf("\n\n\t\t\t\t");
                    printf("1- SADE MOCHA \t\t  70TL \n");
                    printf("\n\t\t\t\t");
                    printf("2- CIKOLATALI MOCHA  \t  75TL \n");

                    printf("\n\n\n\t\t\t\t");
                    printf("Lutfen seciminizi yapiniz: ");

                    secim = _getch();
                    switch (secim)
                    {
                    case '1': {

                        system("CLS");
                        tutar = 70;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet MOCHA  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet MOCHA  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    case '2': {

                        system("CLS");
                        tutar = 75;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet CIKOLATALI MOCHA  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet CIKOLATALI MOCHA  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    default: {
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                        secim = _getch();
                        system("CLS");

                    }
                    }

                } break;

                case '4': {

                    system("CLS");
                    system("Color E0");
                    tutar = 47;
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("Kac adet AMERICANO  istiyorsunuz?");
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t Adet giriniz: ");
                    scanf("%d", &adet);
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    toplamtutar = adet * tutar;
                    printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                    scanf("%d", &odenen);

                    while (odenen < toplamtutar)
                    {
                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                        printf("\n\t\t\t\t\t");
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                        printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                        scanf("%d", &ekodeme);
                        odenen = odenen + ekodeme;
                    }

                    system("CLS");
                    printf("\n\n\n\n\n\t\t\t\t");
                    geriodeme = odenen - toplamtutar;
                    printf(" %d adet AMERICANO  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("Geri odeme: %d TL ", geriodeme);
                    printf("\n\t\t\t\t\t");
                    printf("AFIYET OLSUN. YINE BEKLERIZ");

                    tutar;
                    toplamtutar = 0;
                    odenen = 0;
                    ekodeme = 0;
                    geriodeme = 0;
                    adet = 0;
                    secim = _getch();
                    system("CLS");

                } break;
                case '5': {

                    system("CLS");
                    system("Color E0");
                    tutar = 52;
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("Kac adet CAPPUCINO  istiyorsunuz?");
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t Adet giriniz: ");
                    scanf("%d", &adet);
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    toplamtutar = adet * tutar;
                    printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                    scanf("%d", &odenen);

                    while (odenen < toplamtutar)
                    {
                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                        printf("\n\t\t\t\t\t");
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                        printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                        scanf("%d", &ekodeme);
                        odenen = odenen + ekodeme;
                    }

                    system("CLS");
                    printf("\n\n\n\n\n\t\t\t\t");
                    geriodeme = odenen - toplamtutar;
                    printf(" %d adet CAPPUCINO  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("Geri odeme: %d TL ", geriodeme);
                    printf("\n\t\t\t\t\t");
                    printf("AFIYET OLSUN. YINE BEKLERIZ");

                    tutar;
                    toplamtutar = 0;
                    odenen = 0;
                    ekodeme = 0;
                    geriodeme = 0;
                    adet = 0;
                    secim = _getch();
                    system("CLS");

                } break;
                case '6': {

                    system("CLS");
                    system("Color E0");
                    tutar = 54;
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("Kac adet CAFFE LATTE  istiyorsunuz?");
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t Adet giriniz: ");
                    scanf("%d", &adet);
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    toplamtutar = adet * tutar;
                    printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                    scanf("%d", &odenen);

                    while (odenen < toplamtutar)
                    {
                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                        printf("\n\t\t\t\t\t");
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                        printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                        scanf("%d", &ekodeme);
                        odenen = odenen + ekodeme;
                    }

                    system("CLS");
                    printf("\n\n\n\n\n\t\t\t\t");
                    geriodeme = odenen - toplamtutar;
                    printf(" %d adet CAFFE LATTE  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                    printf("\n\t\t\t\t\t");
                    printf("Geri odeme: %d TL ", geriodeme);
                    printf("\n\t\t\t\t\t");
                    printf("AFIYET OLSUN. YINE BEKLERIZ");

                    tutar;
                    toplamtutar = 0;
                    odenen = 0;
                    ekodeme = 0;
                    geriodeme = 0;
                    adet = 0;
                    secim = _getch();
                    system("CLS");

                } break;
                case '7': {

                    system("CLS");
                    system("Color E0");
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("SICAK CIKOLATA\n");
                    printf("\t\t\t\t");
                    printf("---------------------------------------\n");
                    printf("\n\n\t\t\t\t");
                    printf("1- KAHVELI SICAK CIKOLATA  \t\t  69TL\n");
                    printf("\n\t\t\t\t");
                    printf("2- BEYAZ SICAK CIKOLATA   \t\t  73TL\n");
                    printf("\n\t\t\t\t");

                    printf("\n\n\n\t\t\t\t");
                    printf("Lutfen seciminizi yapiniz: ");

                    secim = _getch();
                    switch (secim)
                    {
                    case '1': {

                        system("CLS");
                        tutar = 69;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet KAHVELI SICAK CIKOLATA  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet KAHVELI SICAK CIKOLATA  icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    case '2': {

                        system("CLS");
                        tutar = 73;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet BEYAZ CIKOLATA  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet BEYAZ CIKOLATA   icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    default: {
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                        secim = _getch();
                        system("CLS");

                    }
                    }

                } break;
                case '8': {

                    system("CLS");
                    system("Color E0");
                    printf("\n\n\n\n\n\t\t\t\t\t");
                    printf("SALEP SEKER SECIMI (seker ucretsizdir)\n");
                    printf("\t\t\t\t");
                    printf("---------------------------------------\n");
                    printf("\n\n\t\t\t\t");
                    printf("1- SEKERLI \n");
                    printf("\n\t\t\t\t");
                    printf("2- SEKERSIZ \n");
                    printf("\n\t\t\t\t");

                    printf("\n\n\n\t\t\t\t");
                    printf("Lutfen seciminizi yapiniz: ");

                    secim = _getch();

                    switch (secim)
                    {

                    case '1': {

                        system("CLS");
                        tutar = 73;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet (sekerli) SALEP  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet (sekerli) SALEP   icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    case '2': {

                        system("CLS");
                        tutar = 73;
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        printf("Kac adet (sekersiz) SALEP  istiyorsunuz?");
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t Adet giriniz: ");
                        scanf("%d", &adet);
                        printf("\n\n\n\n\n\t\t\t\t\t");
                        toplamtutar = adet * tutar;
                        printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("\n\t\t\t\t\tYatiracaginiz ucreti giriniz: ");
                        scanf("%d", &odenen);

                        while (odenen < toplamtutar)
                        {
                            system("CLS");
                            printf("\n\n\n\n\n\t\t\t\t");
                            printf("ODEME MIKTARI YETERSIZ! Lutfen odediginiz miktara ilave ucret yatiriniz: ");
                            printf("\n\t\t\t\t\t");
                            printf("Toplam odemeniz gereken tutar: %d", toplamtutar);
                            printf("\n\t\t\t\t\t");
                            printf("\n Su ana kadar odediginiz miktar: %d", odenen);
                            printf("\n\t\t\t\t\tEk ucreti giriniz: ");
                            scanf("%d", &ekodeme);
                            odenen = odenen + ekodeme;
                        }

                        system("CLS");
                        printf("\n\n\n\n\n\t\t\t\t");
                        geriodeme = odenen - toplamtutar;
                        printf(" %d adet (sekersiz) SALEP   icin %d TL  odemeniz alinmistir.", adet, toplamtutar);
                        printf("\n\t\t\t\t\t");
                        printf("Geri odeme: %d TL ", geriodeme);
                        printf("\n\t\t\t\t\t");
                        printf("AFIYET OLSUN. YINE BEKLERIZ");

                        tutar;
                        toplamtutar = 0;
                        odenen = 0;
                        ekodeme = 0;
                        geriodeme = 0;
                        adet = 0;
                        secim = _getch();
                        system("CLS");

                    } break;
                    default: {
                        printf("\n\n\n\n\n\t\t\t\t");
                        printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                        secim = _getch();
                        system("CLS");

                    }
                    }
                } break;

                default: {
                    printf("\n\n\n\n\n\t\t\t\t");
                    printf(" LUTFEN GECERLI BIR SECIM YAPINIZ(!) ");
                    secim = _getch();
                    system("CLS");

                }

                }

            }

        } while (secim != 27);
        system("CLS");
        printf("\n  Programdan cikmak istediginizden emin misiniz? (E/H)");
        secim = _getch();
        system("CLS");
    } while (secim != 'E' && secim != 'e');
    return 0;

}
