# first
class User{
    static count = 0;
    constructor(username, email, password) {
      this.username = username;
      this.email = email;
      this.password = password;
      User.count++
    }
    printNumberOfUsers(){
        console.log("currentnumberofusers =", User.count)
    }
    

}

class Member extends User {
  constructor(username, email, password ) {
      
    super(username, email, password);     // complete the super function only. Do not make any other changes
    
    this.membershipactivetilldate = new Date(2023, 2, 3)//assume user has joined ur platform on 3rd March
    this.package = '';
  }
  
    //Based on the package bought, increase the membershipactivetilldate
    //Monthly membership increases the va1idity by 1 month
    //Yearly membership increases the va1idity by 1 year
  purchaseMembership(membershippackagename){
    if (membershippackagename === 'YEARLYPACKAGE') {
        this.membershipactivetilldate.setFullYear(this.membershipactivetilldate.getFullYear() + 1);
        this.package='YEARLYPACKAGE ';
    } else {
        this.membershipactivetilldate.setMonth(this.membershipactivetilldate.getMonth() + 1);
        this.package='MONTHLYPACKAGE ';
    }
    //   Complete this function
      
 
  }
}
