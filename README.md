# Simple_Restaurant_System_Core_Java

paste the code below
and add required jar

import java.awt.Container;
import java.awt.event.*;
import javax.swing.*;
import java.applet.Applet;
import java.awt.BasicStroke;
import java.awt.Color;
import java.awt.Dimension;
import java.awt.FlowLayout;
import java.awt.Font;
import java.awt.Graphics;
import java.awt.Graphics2D;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyEvent;
import java.awt.event.MouseEvent;
import java.awt.event.MouseListener;
import java.awt.event.WindowEvent;
import java.awt.event.WindowListener;
import java.io.PrintStream;

import javax.swing.border.Border;

class first extends JFrame
{
	first()
	{
	final JLabel label= new JLabel("       welcome! to our site                  "); 
	label.setBounds(100,50,700,50); 	
	
	
	Container c=getContentPane();
	c.setBackground(Color.pink);
	
	JButton b1=new JButton("Sign-up");
	b1.setBounds(100,150,150,30);
	
	JButton b2=new JButton("Login");
	b2.setBounds(350,150,150,30);
	

	b1.setFont(new Font("chiller",Font.BOLD,30));
	b2.setFont(new Font("chiller",Font.BOLD,30));
	label.setFont(new Font("chiller",Font.BOLD,30));
	
	
	add(label);add(b1);add(b2);

	setSize(800,800);
	setLayout(null);
	setTitle("Site Introduction");
	setVisible(true);
	setLocationRelativeTo(null);
	setResizable(false);
	
	b1.addActionListener
	 ( 
			new ActionListener()
			{
			   public void actionPerformed(ActionEvent e)	
				{
				  try
				  {
                   new third();  
				  }
				  finally {}
				}
			}
	  
	  );
	
	b2.addActionListener
	 (
			new ActionListener()
			{
			   public void actionPerformed(ActionEvent e)	
				{
				   try {
                   new second();
				   }
				   finally {}
				}
			}
	  );
	}

}

class second
{
	second()
	{ 		
		JFrame f=new JFrame("LOGIN PAGE"); 
		
		final JLabel label= new JLabel(); 
		label.setBounds(100,350,700,50); 	
		
		final JPasswordField value = new JPasswordField();
		value.setBounds(350,200,100,30);
		
		Container c=f.getContentPane();
		c.setBackground(Color.pink);
		
		JLabel l1=new JLabel("Username: ");
		l1.setBounds(100,120,500,30);
		
		JLabel l2=new JLabel("Password: ");
		l2.setBounds(100,200,500,30);
		
		JButton b=new JButton("Login");
		b.setBounds(350,280,100,30);
		
		l1.setFont(new Font("chiller",Font.BOLD,30));
		l2.setFont(new Font("chiller",Font.BOLD,30));
		label.setFont(new Font("chiller",Font.BOLD,30));
		
		final JTextField text = new JTextField();
		text.setBounds(350,120,100,30);
		
		f.add(value);f.add(l1);f.add(label);f.add(b);f.add(text);f.add(l2);

		f.setSize(800,800);
		f.setLayout(null);
		f.setLocationRelativeTo(null);
		f.setVisible(true);
		
		
		b.addActionListener
		 (
				new ActionListener()
				{
				   public void actionPerformed(ActionEvent e)	
					{
					   try {
					   String userText;
                       String pwdText;
                       userText = text.getText();
                       pwdText = value.getText();
                         {
                                if (userText.equalsIgnoreCase("KHUSHI") && pwdText.equalsIgnoreCase("12345") || userText.equalsIgnoreCase("AZIZ") && pwdText.equalsIgnoreCase("67890")) 
                                    {
                                      new forth();
                                    }
                                else 
                                    {
                                      JOptionPane.showMessageDialog(f, "Invalid Username or Password");
                                    } 
					     }
				     }
				
				   finally 
				   {
					   
				   }
					}
				}
		  );
		
	}

	
}	

class forth
{
  forth()
	{
			
		JFrame f=new JFrame("MENU BAR"); 
		
		Container c=f.getContentPane();
		c.setBackground(Color.pink);
		
		JButton b1=new JButton(" Menu ");
		b1.setBounds(100,120,150,30);
		
		JButton b2=new JButton(" Feedback ");
		b2.setBounds(100,280,150,30);
		
		JButton b3=new JButton(" Game ");
		b3.setBounds(100,200,150,30);
		
		JLabel b = new JLabel("CLICK THE CROSS BUTTON TO EXIT ");
		b.setBounds(100,500,600,30);
		
		JLabel l1 = new JLabel("PLACE THE ORDER AT 9367238432");
		l1.setBounds(100, 400, 600, 40);
		l1.setFont(new Font("chiller",Font.BOLD,30));
		f.add(l1);
		
		JPanel panel1=new JPanel();
		panel1.setBorder(BorderFactory.createTitledBorder("CENTER"));
		
		b1.setFont(new Font("chiller",Font.BOLD,30));
		b2.setFont(new Font("chiller",Font.BOLD,30));
		b3.setFont(new Font("chiller",Font.BOLD,30));
		b.setFont(new Font("chiller",Font.BOLD,30));
		
		
		f.add(b1);
		f.add(b);
		f.add(b2);
		f.add(b3);


		f.setSize(800,800);
		f.setLayout(null);
		f.setLocationRelativeTo(null);
		f.setVisible(true);
		
		b2.addActionListener
		 (
				new ActionListener()
				{
				   public void actionPerformed(ActionEvent e)	
					{
                      new feedback();
					}
				}
		  );
		b1.addActionListener
		 (
				new ActionListener()
				{
				   public void actionPerformed(ActionEvent e)	
					{
                     new menu();
					}
				}
		  );
		b3.addActionListener
		 (
				new ActionListener()
				{
				   public void actionPerformed(ActionEvent e)	
					{
                     new game();
					}
				}
		  );

                     f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
			
	 }
}


class third
{
	third()
	{		
		JFrame f=new JFrame("sign-up page"); 
		 			
		final JPasswordField value = new JPasswordField();
		value.setBounds(350,360,150,30);
		
		Container c=f.getContentPane();
		c.setBackground(Color.pink);
		
		JLabel l1=new JLabel("Username : ");
		l1.setBounds(100,120,500,30);
		
		JLabel l2=new JLabel("Phone Number :");
		l2.setBounds(100,200,500,30);
		
		JLabel l3=new JLabel("Email :");
		l3.setBounds(100,280,500,30);
		
		JLabel l4=new JLabel("Password : ");
		l4.setBounds(100,360,500,30);
		
		JButton b=new JButton("Login");
		b.setBounds(370,500,100,30);
		
		l1.setFont(new Font("chiller",Font.BOLD,30));
		l2.setFont(new Font("chiller",Font.BOLD,30));
		l3.setFont(new Font("chiller",Font.BOLD,30));
		l4.setFont(new Font("chiller",Font.BOLD,30));
		
		JTextField text = new JTextField();
		text.setBounds(350,120,150,30);
		
		JTextField text1 = new JTextField();
		text1.setBounds(350,200,150,30);
		
		JTextField text2 = new JTextField();
		text2.setBounds(350,280,150,30);
		
		f.add(value);f.add(l1);f.add(b);f.add(text);f.add(l2);f.add(l3);f.add(l4);f.add(text1);f.add(text2);

		f.setSize(800,800);
		f.setLayout(null);
		f.setLocationRelativeTo(null);
		f.setVisible(true);
		
		b.addActionListener
		 (
				new ActionListener()
				{
				   public void actionPerformed(ActionEvent e)	
					{
					   String userText;
                       String pwdText;
					   String pnText;
                       String emText;
                       userText = text.getText();
                       pwdText = value.getText();
                       pnText=text1.getText();
                       emText=text2.getText();
					   if(userText.equalsIgnoreCase("") || pwdText.equalsIgnoreCase("") || emText.equalsIgnoreCase("") || pnText.equalsIgnoreCase(""))
					   {
						   JOptionPane.showMessageDialog(f, "Fill out all Details");  
					   }
					   else
					   {
						   new forth();
					   }
					}
				}
		  );
	 }
}

class feedback implements ActionListener
{
JFrame fr;
JRadioButton rb1,rb2,rb3,rb4;
JButton b1,b2,b;
JLabel lb1,lb2;
ButtonGroup bg;
String ques[]={"Would you like the taste of our food?","Would you enjoy the decorum and the lightning?","How was the prices?","Would you like to come here again?","Would you recommend the restaurant to your friends and relatives"};
String op1[]={"Bad","Bad","low","No","No"};
String op2[]={"Average","Average","Average","Lets see","Lets see"};
String op3[]={"Tasty","Nice","High","Yes","Yes"};
String op4[]={"Very Tasty","Very Nice","Very High","Yes For Sure","Yes For sure"};
int cn;

feedback()
{
fr=new JFrame("Feedback page");
fr.setLayout(null);
fr.setSize(800,800);
Container c=fr.getContentPane();
c.setBackground(Color.pink);
lb1=new JLabel(ques[0]);
lb1.setBounds(50,50,800,30);
fr.add(lb1);
lb1.setFont(new Font("chiller",Font.BOLD,30));
rb1=new JRadioButton(op1[0]);
rb1.setBounds(100,120,100,30);
fr.add(rb1);
rb2=new JRadioButton(op2[0]);
rb2.setBounds(350,120,100,30);
fr.add(rb2);
rb3=new JRadioButton(op3[0]);
rb3.setBounds(100,200,100,30);
fr.add(rb3);
rb4=new JRadioButton(op4[0]);
rb4.setBounds(350,200,100,30);
fr.add(rb4);
bg =new ButtonGroup();
bg.add(rb1);
bg.add(rb2);
bg.add(rb3);
bg.add(rb4);
rb1.addActionListener(this);
rb2.addActionListener(this);
rb3.addActionListener(this);
rb4.addActionListener(this);
b1=new JButton("Sumbit");
b1.setBounds(100,400,100,30);
fr.add(b1);
b2=new JButton("Next");
b2.setBounds(250,400,100,30);
fr.add(b2);
b1.addActionListener(this);
b2.addActionListener(this);
fr.setLocationRelativeTo(null);
fr.setVisible(true);


JButton b=new JButton("  Back ");
b.setBounds(170,600,130,50);

b.setFont(new Font("chiller",Font.BOLD,30));
fr.add(b);


b.addActionListener
(
		new ActionListener()
		{
		   public void actionPerformed(ActionEvent e)	
			{
              new forth();
			}
		}
 );
}

public void actionPerformed(ActionEvent e)
{
if(e.getSource()==b1)
{
String en="";
if(rb1.isSelected())
en=rb1.getText();
if(rb2.isSelected())
en=rb2.getText();
if(rb3.isSelected())
en=rb3.getText();
if(rb4.isSelected())
en=rb4.getText();
JOptionPane.showMessageDialog(null,"thanks! for your feedback");
}
if (e.getSource()==b2)
{
cn++;
lb1.setText(ques[cn]);
rb1.setText(op1[cn]);
rb2.setText(op2[cn]);
rb3.setText(op3[cn]);
rb4.setText(op4[cn]);
}
}
}
 

class game extends Applet
implements MouseListener, ActionListener
{
    JFrame f;
    int flag = 2;
    int n;
    int m;
    int i = 0;
    static int bug = 0;
    char[] ch = new char[9];
    JButton first;
    JButton second;
    String s1 = "";
    
    public game()
    {
        f = new JFrame("Tic Tac Toe");
        first = new JButton("CLEAR");
        second = new JButton("EXIT");
        f.add(first);
        f.add(second);

    	f.setLocationRelativeTo(null);
    	
        f.getContentPane().setBackground(Color.pink);
        f.setLayout(null);
        f.setVisible(true);
        f.setSize(800, 800);
        first.setBounds(650, 50, 90, 60);
        second.setBounds(650, 250, 90, 60);
        
        f.addMouseListener(this);
        for (i = 0;i < 9;i += 1)
        ch[i] = 'B';
        first.addActionListener(this);
        second.addActionListener(this);
        
        String message = "Please click on the frame   !!!!! \n    \nto start the game \n";
        
        JOptionPane pane = new JOptionPane(message);
        JDialog dialog = pane.createDialog(new JFrame(), "Dialog");
        dialog.show();
        Graphics g = f.getGraphics();
        g.drawLine(200, 0, 200, 600);
        g.drawLine(400, 0, 400, 600);
        g.drawLine(0, 200, 600, 200);
        g.drawLine(0, 400, 600, 400);
        g.drawLine(600, 0, 600, 600);
        g.drawLine(0, 600, 600, 600);
    }
    
    public void keyPressed(KeyEvent k)
    {
        System.out.print("");
    }
    
    public void keyTyped(KeyEvent k) {
        s1 += k.getKeyChar();
    }
    
    public void keyReleased(KeyEvent k) {
        System.out.print("");
    }
    
    public void actionPerformed(ActionEvent ae)
    {
        if (ae.getSource() == first)
        {
            f.setVisible(false);
            bug = 0;
            new game();
        }
        if (ae.getSource() == second)
        {
            new forth();
        }
    }
    
    public void mouseClicked(MouseEvent e)
    { 
    	Graphics2D g2;
        Graphics g = f.getGraphics();
        g.drawLine(200, 0, 200, 600);
        g.drawLine(400, 0, 400, 600);
        g.drawLine(0, 200, 600, 200);
        g.drawLine(0, 400, 600, 400);
        g.drawLine(600, 0, 600, 600);
        flag -= 1;
        int x = e.getX();
        int y = e.getY();
        if (flag == 1)
        {
            if ((x < 200) && (y < 200)) { m = 0; n = 0; ch[0] = 'R'; }
            if ((x > 200) && (x < 400) && (y < 200)) { m = 200; n = 0; ch[1] = 'R'; }
            if ((x > 400) && (x < 600) && (y < 200)) { m = 400; n = 0; ch[2] = 'R'; }
            if ((x < 200) && (y > 200) && (y < 400)) { m = 0; n = 200; ch[3] = 'R'; }
            if ((x > 200) && (x < 400) && (y > 200) && (y < 400)) { m = 200; n = 200; ch[4] = 'R'; }
            if ((x > 400) && (x < 600) && (y > 200) && (y < 400)) { m = 400; n = 200; ch[5] = 'R'; }
            if ((x < 200) && (y > 400) && (y < 600)) { m = 0; n = 400; ch[6] = 'R'; }
            if ((x > 200) && (x < 400) && (y > 400) && (y < 600)) { m = 200; n = 400; ch[7] = 'R'; }
            if ((x > 400) && (x < 600) && (y > 400) && (y < 600)) { m = 400; n = 400; ch[8] = 'R'; }
            g.setColor(new Color(77, 176, 230));
            g2 = (Graphics2D)g;
            g2.setStroke(new BasicStroke(10.0F));
            g.drawOval(m + 10, n + 10, 159, 159);
        }
        
        if (flag == 0)
        {
            if ((x < 200) && (y < 200)) { m = 0; n = 20; ch[0] = 'P'; }
            if ((x > 200) && (x < 400) && (y < 200)) { m = 200; n = 20; ch[1] = 'P'; }
            if ((x > 400) && (x < 600) && (y < 200)) { m = 400; n = 20; ch[2] = 'P'; }
            if ((x < 200) && (y > 200) && (y < 400)) { m = 0; n = 200; ch[3] = 'P'; }
            if ((x > 200) && (x < 400) && (y > 200) && (y < 400)) { m = 200; n = 200; ch[4] = 'P'; }
            if ((x > 400) && (x < 600) && (y > 200) && (y < 400)) { m = 400; n = 200; ch[5] = 'P'; }
            if ((x < 200) && (y > 400) && (y < 600)) { m = 0; n = 400; ch[6] = 'P'; }
            if ((x > 200) && (x < 400) && (y > 400) && (y < 600)) { m = 200; n = 400; ch[7] = 'P'; }
            if ((x > 400) && (x < 600) && (y > 400) && (y < 600)) { m = 400; n = 400; ch[8] = 'P'; }
            g2 = (Graphics2D)g;
            g2.setStroke(new BasicStroke(10.0F));
            g.setColor(new Color(77, 176, 230));
            g.drawLine(m + 10, n + 13, m + 169, n + 164);
            g.drawLine(m + 169, n + 10, m + 10, n + 169);
            flag += 2;
        }
        
        for (i = 0; i < 3; i += 1)
        {
            if ((ch[i] != 'B') &&
            (ch[(i + 3)] == ch[i]) && (ch[(i + 6)] == ch[i]))
            {
                new Board().win();
                bug = 1;
            }
        }
        
        for (i = 0; i < 7;i += 1)
        {
            if (ch[i] != 'B')
            {
                if ((ch[i] == ch[(i + 1)]) && (ch[i] == ch[(i + 2)]))
                {
                    new Board().win();
                    bug = 1;
                }
                i += 2;
            }
            else {
                i += 2;
            }
        }
        if ((ch[4] != 'B') && ((
        ((ch[0] == ch[4]) && (ch[4] == ch[8])) || ((ch[2] == ch[4]) && (ch[4] == ch[6])))))
        {
            new Board().win();
            bug = 1;
        }
        
        for (i = 0; (i < 9) &&
        (ch[i] != 'B'); i += 1)
        {
            if (i == 8)
            {
                if (bug == 0)
                new Board().draw();
                bug = 0;
            }
        }
    }
    
    public void mouseReleased(MouseEvent e)
    {
        System.out.print("");
    }
    
    public void mouseEntered(MouseEvent e)
    {
        System.out.print("");
    }
    
    public void mouseExited(MouseEvent e) {
        System.out.print("");
    }
    
    public void mousePressed(MouseEvent e) {
        System.out.print("");
    }
    
}


class Board  implements WindowListener
{
    public void win()
    {
        String message = "Congratulations !!!!! \n    \nYou win \n";
        
        JOptionPane pane = new JOptionPane(message);
        JDialog dialog = pane.createDialog(new JFrame(), "Dialog");
        dialog.show();
    }
    
    public void draw()
    {
        String message = "Players the result is  !!!!! \n    \nSTALEMATE \n";
        
        JOptionPane pane = new JOptionPane(message);
        JDialog dialog = pane.createDialog(new JFrame(), "Dialog");
        dialog.show();
    }
    
    public void windowClosing(WindowEvent we)
    {
        System.exit(0);
    }
}


class menu
{	
     JFrame f1;  
     JMenuBar mb;
     JLabel l1;
     
 JMenu BIRYANIS,STARTERS,KEBABS,BEVERAGES,SPECIAL_BISCUITS,DESSERTS,CURRIES,INDIAN_BREADS;
 JMenuItem Tandoori_Roti, Plain_Naan, Butter_Roti, RoyalChickenBiryani, Garlic_Naan, Butter_Naan, Gajar_Ka_Halwa , dal_fry, dal_makhani, egg_masala, butter_chicken_boneless, chicken_tikka_masala, Osmania_Biscuit_Box, Special_Biscuit_Box, Double_Ka_Meetha, Gulab_Jamun, Qubani_Ka_Meetha, RoyalMuttonBiryani, VegBiryani, VegFamilyPack, ChickenFamilyPack, ChilliChicken, Paneer65, VegManchurian, ChickenTikkaKebab, TandooriChicken, ChickenGarlicKebab, DietCoke, MineralWater, Sprite, Fanta, Maaja;
  
 
 menu() 
 {
    f1 = new JFrame("Restaurant menu");
	mb= new JMenuBar();
	BIRYANIS =new JMenu("BIRYANIS");
	STARTERS =new JMenu("STARTERS");
	KEBABS =new JMenu("KEBABS");	
	BEVERAGES =new JMenu("BEVERAGES");
	SPECIAL_BISCUITS=new JMenu("SPECIAL BISCUITS");
	DESSERTS=new JMenu("DESSERTS");
	CURRIES=new JMenu("CURRIES");
	INDIAN_BREADS=new JMenu("INDIAN BREADS");
	
	RoyalChickenBiryani = new JMenuItem("Royal Chicken Biryani____199");
	RoyalMuttonBiryani = new JMenuItem("royal Mutton Biryani______219");	
	VegBiryani = new JMenuItem("Veg Biryani______219");
	DietCoke = new JMenuItem("Diet Coke______50");	
	MineralWater = new JMenuItem("Mineral Water______20");	
	VegFamilyPack = new JMenuItem("Veg Family Pack______429");
	ChickenFamilyPack = new JMenuItem("Chicken Family Pack______619");	
	ChilliChicken = new JMenuItem("Chilli Chicken______264");	
	Paneer65 = new JMenuItem("Paneer 65______196");
	VegManchurian = new JMenuItem("Veg Manchurian______189");	
	ChickenGarlicKebab = new JMenuItem("Chicken Garlic Kebab______243");	
	ChickenTikkaKebab = new JMenuItem("chicken Tikka Kebab______243");
	TandooriChicken = new JMenuItem("Tandoori Chicken______379");	
	Sprite = new JMenuItem("Sprite______35");	
	Maaja = new JMenuItem("Maaja______35");	
	Fanta = new JMenuItem("Fanta______40");	
	Osmania_Biscuit_Box = new JMenuItem("Osmania Biscuit Box______124");
	Special_Biscuit_Box = new JMenuItem("Special Biscuit Box______176");
	Double_Ka_Meetha = new JMenuItem("Double Ka Meetha_______99");
	Gulab_Jamun = new JMenuItem("Gulab Jamun______99");
	Qubani_Ka_Meetha = new JMenuItem("Qubani Ka Meetha______139");
	Gajar_Ka_Halwa = new JMenuItem("Gajar Ka Halwa_____119");
	dal_fry = new JMenuItem("Dal Fry_____219");
	dal_makhani = new JMenuItem("Dal Makhani______219"); 
	egg_masala = new JMenuItem("Egg Masala_____209");
	butter_chicken_boneless = new JMenuItem("Butter Chicken Boneless_____329");
	chicken_tikka_masala = new JMenuItem("Chicken Tikka Masala_____329");
	Tandoori_Roti = new JMenuItem("Tandoori Roti_____49");
	Butter_Roti = new JMenuItem("Butter Roti______63");
	Plain_Naan = new JMenuItem("Plain Naan______63");
	Butter_Naan = new JMenuItem("Butter_Naan_____72");
	Garlic_Naan = new JMenuItem("Garlic_Naan____72");
	
	BIRYANIS.add(RoyalChickenBiryani);
	BIRYANIS.add(RoyalMuttonBiryani);
	BIRYANIS.add(VegBiryani);
	BIRYANIS.add(VegFamilyPack);
	BIRYANIS.add(ChickenFamilyPack);
	STARTERS.add(ChilliChicken);
	STARTERS.add(VegManchurian);
	STARTERS.add(Paneer65);
    KEBABS.add(ChickenTikkaKebab);
    KEBABS.add(ChickenGarlicKebab);
    KEBABS.add(TandooriChicken);
	BEVERAGES.add(Sprite);
	BEVERAGES.add(Maaja);
	BEVERAGES.add(Fanta);
	BEVERAGES.add(DietCoke);
	BEVERAGES.add(MineralWater);
	SPECIAL_BISCUITS.add(Special_Biscuit_Box);
	SPECIAL_BISCUITS.add(Osmania_Biscuit_Box);
	DESSERTS.add(Double_Ka_Meetha);
	DESSERTS.add(Gulab_Jamun);
	DESSERTS.add(Qubani_Ka_Meetha);
	DESSERTS.add(Gajar_Ka_Halwa);
	CURRIES.add(dal_fry);
	CURRIES.add(dal_makhani);
	CURRIES.add(egg_masala);
	CURRIES.add(butter_chicken_boneless);
	CURRIES.add(chicken_tikka_masala);
	INDIAN_BREADS.add(Tandoori_Roti);  
	INDIAN_BREADS.add(Butter_Roti);  
	INDIAN_BREADS.add(Plain_Naan);  
	INDIAN_BREADS.add(Butter_Naan);  
	INDIAN_BREADS.add(Garlic_Naan);  
		
    mb.add(BIRYANIS);
    mb.add(STARTERS);
    mb.add(KEBABS);
    mb.add(BEVERAGES);
    mb.add(SPECIAL_BISCUITS);
    mb.add(DESSERTS);
    mb.add(CURRIES);
    mb.add(INDIAN_BREADS);
	
	f1.setJMenuBar(mb);	
	f1.setSize(800, 800);
	f1.setVisible(true);
	f1.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
 
	Container c=f1.getContentPane();
	c.setBackground(Color.pink);
	
    JButton b=new JButton("      Back     ");
    b.setBounds(350,750,500,40);
    b.setFont(new Font("chiller",Font.BOLD,30));
	f1.add(b);
	
	
	b.addActionListener
	 (
			new ActionListener()
			{
			   public void actionPerformed(ActionEvent e)	
				{
                 new forth();
				}
			}
	  );
	
 }  

}

public class restaurant
{
	public static void main(String[] args)
	 {  	
		new first();
	 }
}

