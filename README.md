# Pattern_generator

# How to use
## 1. Capture signal
##### pin map
![image](https://github.com/user-attachments/assets/6cfa90a1-47f2-4064-832b-53817231e64e)
##### test signal
![image](https://github.com/user-attachments/assets/6953bd1d-6e24-41d6-a1d1-aeb8747cda20)

## 2. Make csv to excel
![image](https://github.com/user-attachments/assets/e0123698-ec10-4304-a6e0-22d612fa9087)

## 3. Make excel to data pattern
**⚠️ 주의:** You must open and save the generated *.xlsx file manually before creating the data pattern.
#### 3-1. make single pattern file (gpio + peri)
![image](https://github.com/user-attachments/assets/861551eb-540c-4aed-bab9-a7e186105b7d)
![image](https://github.com/user-attachments/assets/31408f4b-84d0-46b0-b389-ea424d73cf2a)
```
	W "T1"; V { all_pin	=	1 0 0 0 0 0 X X X X X X X X X X X X X X X X X ;} // 0, 0ns                        // input
	W "T1"; V { all_pin	=	0 0 0 0 0 0 X X X X X X X X X X X X X X X X X ;} // 1400, 7000ns                  // input
	W "T1"; V { all_pin	=	H L L L L L L L L L L L L L L L L L L L L L L ;} // 3200, 16000ns                 // output
	W "T1"; V { all_pin	=	L H L L L L L L L L L L L L L L L L L L L L L ;} // 8050, 40250ns
	W "T1"; V { all_pin	=	L L H L L L L L L L L L L L L L L L L L L L L ;} // 12050, 60250ns
	W "T1"; V { all_pin	=	L L L H L L L L L L L L L L L L L L L L L L L ;} // 16050, 80250ns
	W "T1"; V { all_pin	=	L L L L H L L L L L L L L L L L L L L L L L L ;} // 20050, 100250ns
	W "T1"; V { all_pin	=	L L L L L H L L L L L L L L L L L L L L L L L ;} // 24050, 120250ns
	W "T1"; V { all_pin	=	L L L L L L H L L L L L L L L L L L L L L L L ;} // 28050, 140250ns
	W "T1"; V { all_pin	=	L L L L L L L H L L L L L L L L L L L L L L L ;} // 32050, 160250ns
	W "T1"; V { all_pin	=	L L L L L L L L H L L L L L L L L L L L L L L ;} // 36050, 180250ns
	W "T1"; V { all_pin	=	L L L L L L L L L H L L L L L L L L L L L L L ;} // 40050, 200250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L H L L L L L L L L L L L L ;} // 44050, 220250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L H L L L L L L L L L L L ;} // 48050, 240250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L L H L L L L L L L L L L ;} // 52050, 260250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L L L H L L L L L L L L L ;} // 56050, 280250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L L L L H L L L L L L L L ;} // 60050, 300250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L L L L L H L L L L L L L ;} // 64050, 320250ns
	W "T1"; V { all_pin	=	L L L L L L L L L L L L L L L L H L L L L L L ;} // 68050, 340250ns
                                         ... 
```

#### 3-2. make separate pattern file (gpio / peri)
![image](https://github.com/user-attachments/assets/836dbba6-9580-4b23-b42b-6834644a2c08)
![image](https://github.com/user-attachments/assets/164357b8-8384-4867-ae73-607eeeedffec)

ℹ️ **Note:** margin : add margin before output signal

## 4. Fill mask pattern
![image](https://github.com/user-attachments/assets/4de281c0-c985-4e65-a10f-3d898ce56fc8)
![image](https://github.com/user-attachments/assets/2924182c-541e-40d7-8368-d2ac79a5ad11)

```
	W "T1"; V { all_pin	=	1 0 0 0 0 0 X X X X X X X X X X X X X X X X X ;} // 0, 0ns                        // input
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 1, 5ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 2, 10ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 3, 15ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 4, 20ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 5, 25ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 6, 30ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 7, 35ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 8, 40ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 9, 45ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 10, 50ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 11, 55ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 12, 60ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 13, 65ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 14, 70ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 15, 75ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 16, 80ns                        // fill mask
	W "T1"; V { all_pin =	X X X X X X X X X X X X X X X X X X X X X X X ;} // 17, 85ns                        // fill mask
                                         ... 
```

