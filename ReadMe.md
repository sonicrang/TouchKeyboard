调用方法：可以直接在该项目下操作，也可以把上面代码生成dll，引用到其他项目。使用时可以通过xaml关联或者动态设置。

**一、XAML关联方式：**

1.在Xaml页面设置k

xmlns:k="clr-namespace:TouchKeyboard.Keyboard;

2.TextBox控件或者Password中加入代码 k:TouchScreenKeyboard.TouchScreenKeyboard="True"

例如：

    
      <TextBox k:TouchScreenKeyboard.TouchScreenKeyboard="True" HorizontalAlignment="Left"  Height="31" Margin="66,22,0,0" TextWrapping="Wrap" Text="" VerticalAlignment="Top" Width="373" FontSize="16"/>




3.运行程序，当文本框获得焦点时弹出虚拟键盘。（仅支持TextBox和PassWord控件）



**二、动态关联**

通过SetValue直接操作DependencyProperty设置value为true即可

例如

    
       txtUser.SetValue(TouchKeyboard.Keyboard.TouchScreenKeyboard.TouchScreenKeyboardProperty, true);


反之，如果要取消关联，就设置为false.
