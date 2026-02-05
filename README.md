## 2월 6일

1~7, 11 폼 디자인

<br>

#### [datafiles, Setting.jar, 문제지](https://drive.google.com/file/d/1ETeUsw9BxpnnpwkESPEERE3CjN1tIltc/view?usp=sharing)
#### ▲클릭하면 구글 드라이브에 연결되어있음


---

**[코드]**

▼ main 이미지 슬라이드
```
img1.setIcon(new ImageIcon(new ImageIcon("./datafiles/main/"+i1+".png").getImage().getScaledInstance(400,230,Image.SCALE_SMOOTH)));
	img2.setIcon(new ImageIcon(new ImageIcon("./datafiles/main/"+i2+".png").getImage().getScaledInstance(400,230,Image.SCALE_SMOOTH)));
	Timer timer1=new Timer();
	TimerTask task1=new TimerTask() {
		int x=0;
		@Override
		public void run() {
			// TODO Auto-generated method stub
			x-=5;
			if(x<=-400) {
				x=0;
				
				i1++;
				i2++;
				if(i1==6) {
					i1=1;
				}
				if(i2==6) {
					i2=1;
				}
				
				img1.setIcon(new ImageIcon(new ImageIcon("./datafiles/main/"+i1+".png").getImage().getScaledInstance(400,230,Image.SCALE_SMOOTH)));
				img2.setIcon(new ImageIcon(new ImageIcon("./datafiles/main/"+i2+".png").getImage().getScaledInstance(400,230,Image.SCALE_SMOOTH)));
			}
			img1.setLocation(x, 0);
			img2.setLocation(x+400, 0);
		}
	};
	timer1.schedule(task1, 0, 10);
```

▼ 자격증 목록 폼, 기출문제 맛보기(pdf 실행)
```
try{
    Desktop.getDesktop.open(new File("./datafiles/question/(파일명)/1.pdf"));
}catch(){
}
```

▼ 시험일정 폼, 날짜 더하기
```
LocalDate date=LocalDate.parse("2025-10-25");
date.plusday(7);
```
