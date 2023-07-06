# # Angular引入antd

1、进入angular执行以下命令后将自动完成 ng-zorro-antd 的初始化配置，包括引入国际化文件，导入模块，引入样式文件等工作。

```
$ ng add ng-zorro-antd
```

2、引入特定组件，如button按钮

module.ts页面

```ts
import { NgModule } from '@angular/core';
import { HomeComponent } from './home.component';
import { NzButtonModule } from 'ng-zorro-antd/button';

@NgModule({
  imports: [
    NzButtonModule
  ],
  declarations: [HomeComponent],
  exports: [HomeComponent]
})
export class HomeModule { }
```

html页面

```html
    <button nz-button nzType="primary">Primary Button</button>
    <button nz-button nzType="default">Default Button</button>
    <button nz-button nzType="dashed">Dashed Button</button>
    <button nz-button nzType="text">Text Button</button>
    <a nz-button nzType="link">Link Button</a>
```

表格使用（登录页面）

```ts
import { NgModule } from '@angular/core';
import { LoginComponent } from './login.component';
//路由
import { loginRoutingModule } from './login-routing.module';
//引入zorro-antd使用的组件
import { DemoNgZorroAntdModule } from 'src/app/ng-zorro-antd.module';
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
  imports: [
    loginRoutingModule,
    DemoNgZorroAntdModule,
    ReactiveFormsModule
  ],
  declarations: [LoginComponent],
  exports: [LoginComponent]
})
export class LoginModule { }

```
ng-zorro表单使用时 除需引入ng-zorro的form组件同时需要引入angular的form

需要使用NGif、NgFor等指令需要导入下边模块

``` ts
import { CommonModule } from '@angular/common';

```

# 备注

使用ng-zorro库时，根组件需创建module页面，引入ng-zorro需要module且导入如Login:

login.module.ts
```ts
import { DemoNgZorroAntdModule } from 'src/app/ng-zorro-antd.module';
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
  imports: [
    loginRoutingModule,
    DemoNgZorroAntdModule,
    ReactiveFormsModule
  ],
  declarations: [LoginComponent],
  exports: [LoginComponent]
})
export class LoginModule { }

```
login-routing.module.ts

```ts
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { LoginComponent } from './login.component';

const routes: Routes = [
  {
    path: '', component: LoginComponent,
  },
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class loginRoutingModule { }

```

路由页面需要引入LoginModule 

app.module.ts
```ts
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [
  { path: 'login', loadChildren: () => import('./pages/login/login.module').then(m => m.LoginModule)},
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }

```
