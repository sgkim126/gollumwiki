# dll
## dll 만들기
        #ifdef __cplusplus
        #define EXPORT extern "C" __declspec(dllexport)
        #else
        #define EXPORT __declspec(dllexport)
        #endif

        EXPORT int tmp()
        {
            return 0;
        }

## dll 사용하기
        #include <stdio.h>
        #include <windows.h>

        #define DllName TEXT("bdll.dll")
        #define DllFuncName "tmp"

        typedef int (*PFUNC)();

        int main()
        {
            HMODULE hModule = NULL;
            FARPROC pFunc = NULL;
            PFUNC pSum = NULL;

            hModule = LoadLibrary(DllName);
            if(!hModule) {
                printf("error\n");
                return 0;
            }

            pFunc = GetProcAddress(hModule,DllFuncName);
            pTmp = (PFUNC)pFunc;

            if(!pFunc) {
                printf("Error");
                return 0;
            }
            printf("%d\n",pTmp());
            FreeLibrary(hModule);
            return 0;
        }
