# 2월 4일
오늘 9번 고객센터 폼과 10번 자격증 폼 만들거예요.

9번 할 수 있는 만큼 디자인하고 있으세요.


#### [datafiles, Setting.jar, 문제지](https://drive.google.com/file/d/1ETeUsw9BxpnnpwkESPEERE3CjN1tIltc/view?usp=sharing)

#### ▲클릭하면 구글 드라이브에 연결되어있음




```
DefaultTableCellRenderer dtc=new DefaultTableCellRenderer() {
			@Override
			public Component getTableCellRendererComponent(JTable table, Object value, boolean isSelected,
					boolean hasFocus, int row, int column) {
				// TODO Auto-generated method stub
				Component cmp=null;
				if(column==2) {
					JLabel lb=new JLabel(new ImageIcon(new ImageIcon("./datafiles/icon/locker2.png").getImage().getScaledInstance(20, 20, Image.SCALE_SMOOTH)));
					lb.setText("문의 내용입니다.");
					lb.setFont(getFont().deriveFont(15));
					cmp=lb;
				}
				return cmp;
			}
		};
		table.getColumn(co[2]).setCellRenderer(dtc);
		table.setShowGrid(false);
		jsp.setBorder(BorderFactory.createEmptyBorder());
```
