# Google Service

### Module usage

```
import { GoogleAuthService } from "ng-gapi";

```

### function usage
```
  loginWithGoogle() {
    this.googleAuth.getAuth()
      .subscribe((auth) => {
        auth.signIn().then((res: any) => {
          this.authService.SignWithGoogle(res.vu.jv, res.vu.jf, this.userGuestId).subscribe(
            () => {
              this.checkLogin(this.userGuestUsername, "123456");
            }
          );
        });
      });
  }
 ```
 
### Service usage 
```
   SignWithGoogle(email, name, userId): Observable<any> {
    return this.http.post<any>(environment.API_URL + '/api/auth/local/checkEmail', {
      NAME : name,
      EMAIL : email,
      USER_ID: userId
    });
  }
}
```
 
 

```
    vu
    ├── IX                    "get name of gmail"
    ├── RM                    "https://lh3.googleusercontent.com/a/AATXAJxl"
    ├── YV                    "get familyname of gmail"
    ├── jf                    "name familyname"
    ├── jv                    "gmail"
    └── sW      	      "1xxxxxxx3416140528817"


    wc
    ├── access_token                   
    ├── expires_at                    
    ├── expires_in                    
    ├── first_issued_at                 	  
    ├── id_token               	  
    ├── idpId                
    ├── login_hint               	   
    └── scope                 
	
```
