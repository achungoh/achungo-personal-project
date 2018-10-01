# achungo-personal-project
import javax.swing.*; 
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;


public final class LoginFrame extends JFrame implements ActionListener {
    Container container =getContentPane();
    JLabel userLabel= new JLabel("USERNAME");
    JLabel passwordLabel= new JLabel("PASSWORD");
    JTextField userTextField=new JTextField();
    JPasswordField passwordField=new JPasswordField();
    JButton LoginButton=new JButton("LOGIN");
    JButton resetButton=new JButton("RESET");
    JCheckBox showPassword= new JCheckBox("Show Password");
    
    
    LoginFrame()
            
            
            
            
    {
     setLayoutManager();
     setLocationAndSize();
     addComponentsToContainer();
    }
    public void setLayoutManager()
            {
                container.setLayout(null);
            }
    public void setLocationAndSize()
    {
        userLabel.setBounds(50,150,100,30);
        passwordLabel.setBounds(50,220,100,30);
        userTextField.setBounds(150,150,150,30);
        passwordField.setBounds(150,220,150,30);
        showPassword.setBounds(150,250,150,30);
        LoginButton.setBounds(50,300,100,30);
        resetButton.setBounds(200,300,100,30);
    }
    public void addComponentsToContainer()
    {
     container.add(userLabel);
     container.add(passwordLabel);
     container.add(userTextField);
     container.add(passwordField);
     container.add(LoginButton);
     container.add(resetButton);
     container.add(showPassword);
     
        
        
    }
    public void actionPerfomed(ActionEvent e) {
        
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        
        if(e.getSource()==LoginButton){
            String userText;
            String pwdText;
            userText=userTextField.getText();
            pwdText=passwordField.getText();
            if(userText.equalsIgnoreCase("achungo")&&pwdText.equalsIgnoreCase("12345")){
                JOptionPane.showMessageDialog(this,"Login Successful");
            }else{
                JOptionPane.showMessageDialog(this,"Invalid Username or Password");
            }
        }
        if(e.getSource()==resetButton){
            userTextField.setText("");
            passwordField.setText("");
            
        }
        if(e.getSource()==showPassword){
            if(showPassword.isSelected()){
                passwordField.setEchoChar((char)0);
            }else{
                passwordField.setEchoChar('*');
            }
            
            }
            
            
    }
        
    }


class Loginlogout {

    
    public static void main(String[] args) {
        LoginFrame frame= new LoginFrame();
        frame.setTitle("Login Form");
        frame.setVisible(true);
        frame.setBounds(10,10,370,600);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setResizable(false);
    }
    
}

USER REGISTRATION FORM
import java.awt.*;
import java.awt.event.*;

public class UserDataEntry {
  public static void main(String[] args) {
  Frame frm=new Frame("DataEntry frame");
  Label lbl = new Label("Enter All Fields.");
  frm.add(lbl);
  frm.setSize(350,200);
  frm.setVisible(true);
  frm.addWindowListener(new WindowAdapter(){
  public void windowClosing(WindowEvent e){
  System.exit(0);
  }
  });
  Panel p = new Panel();
  Panel p1 = new Panel();
  
  Label jFirstName = new Label("First Name");
  TextField lFirstName = new TextField(20);
  Label jLastName =new Label("Last Name");
  TextField lLastName=new TextField(20);
  Label jEmail=new Label("Email");
  TextField lEmail=new TextField(20);
  Label jGender=new Label("Gender");
  TextField lGender=new TextField(20);
  TextField lPhoneNumber=new TextField(20);
  Label jPhoneNumber=new Label("Phone Number");
  
  p.setLayout(new GridLayout(6,1));
  
  p.add(jFirstName);
  p.add(lFirstName);
  p.add(jLastName);
  p.add(lLastName);
  p.add(jEmail);
  p.add(lEmail);
  p.add(jPhoneNumber);
  p.add(lPhoneNumber);
  p.add(jGender);
  p.add(lGender);
  
  Button AddUser=new Button("Add User");
  p.add(AddUser);
  p1.add(p);
  frm.add(p1,BorderLayout.NORTH);
  }
} 


