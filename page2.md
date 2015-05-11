#WebSite2

ASP.NET Validator kullanımı

```html
<asp:Label ID="Label1" runat="server" Text="Ad:" Width="50px" />
<asp:TextBox ID="TextBox1" runat="server" />
<asp:RequiredFieldValidator ID="RequiredFieldValidator1" runat="server"
                            ControlToValidate="TextBox1" Display="None"
                            ErrorMessage="Adı giriniz..." /> <br />


<asp:Label ID="Label2" runat="server" Text="Soyad:" Width="50px" />
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator2" runat="server"
                            ControlToValidate="TextBox2" Display="None"
                            ErrorMessage="Soyadı giriniz..." /> <br />


<asp:Label ID="Label3" runat="server" Text="email" Width="50px" />
<asp:TextBox ID="TextBox3" runat="server"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator3" runat="server"
                            ControlToValidate="TextBox3" Display="None"
                            ErrorMessage="email i giriniz..." />
<asp:RegularExpressionValidator ID="RegularExpressionValidator1" runat="server"
                                ControlToValidate="TextBox3" Display="None"
                                ErrorMessage="email hatalı..."
                                ValidationExpression="\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*" /> <br />


<asp:Label ID="Label4" runat="server" Text="Yaş:" Width="50px"></asp:Label>
<asp:TextBox ID="TextBox4" runat="server"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator4" runat="server"
                            ControlToValidate="TextBox4" Display="None"
                            ErrorMessage="yaşı giriniz..." />
<asp:RangeValidator ID="RangeValidator1" runat="server"
                    ControlToValidate="TextBox5" Display="None"
                    ErrorMessage="yaş bilgisi hatalı..." MaximumValue="120"
                    MinimumValue="0" Type="Integer" /> <br />


<asp:Label ID="Label5" runat="server" Text="Şifre" Width="100px"></asp:Label>
<asp:TextBox ID="TextBox5" runat="server" TextMode="Password"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator5" runat="server"
                            ControlToValidate="TextBox5" Display="None"
                            ErrorMessage="şifreyi girin..." />
<asp:CompareValidator ID="CompareValidator1" runat="server"
                      ControlToCompare="TextBox5" ControlToValidate="TextBox6"
                      Display="None" ErrorMessage="şifre hatalı..." /> <br />


<asp:Label ID="Label6" runat="server" Text="Şifre (Tekrar)" Width="100px"></asp:Label>
<asp:TextBox ID="TextBox6" runat="server" TextMode="Password"></asp:TextBox>
<asp:RequiredFieldValidator ID="RequiredFieldValidator6" runat="server"
                            ControlToValidate="TextBox6" Display="None"
                            ErrorMessage="şifreyi girin..." /> <br />


<asp:Button ID="Button1" runat="server" Text="Kayıt" />
<asp:ValidationSummary ID="ValidationSummary1" runat="server" />
```
