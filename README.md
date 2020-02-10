# create new angular application
ng new angular-fblogincd ./angular-fblogin 

#fblogin
cd./angular-flogin
ng serve

#install and configure the angular-social module
npm install --save angularx-social-login

#register the module to the src/app/app.module.ts
import { SocialLoginModule, AuthServiceConfig, FacebookLoginProvider } from 'angularx-social-login';
#declare constant variable and export as the module before the @NgModule line 
const config = new AuthServiceConfig([
  {
    id: FacebookLoginProvider.PROVIDER_ID,
    provider: new FacebookLoginProvider('2203659926599837')
  }
]);

export function provideConfig() {
  return config;
}
