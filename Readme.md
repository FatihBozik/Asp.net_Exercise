#Asp.NET Web Forms

TextBox kullanımı
```html
<p>İsim
  <asp:TextBox ID ="TextBox1" runat="server"
               Height="15px" Width="80px" />
</p>

<asp:Button ID="Button1" runat="server"
            onclick="Button1_Click" Text="Göster" />

<p>
<asp:Literal ID="Literal1" runat="server" />
</p>
```

```csharp
protected void Button1_Click(object sender, EventArgs e)
{
    Literal1.Text = TextBox1.Text;
}
```

<br/><br/>

DropDownList kullanımı
```html
<asp:DropDownList ID="DropDownList1" runat="server"
                  AutoPostBack="True" onselectedindexchanged="DropDownList1_SelectedIndexChanged">

        <asp:ListItem>Fatih</asp:ListItem>
        <asp:ListItem>Bozik</asp:ListItem>
        <asp:ListItem>İstanbul Üniversitesi</asp:ListItem>
        <asp:ListItem>Bilgisayar Mühendisliği</asp:ListItem>

</asp:DropDownList>

<p>
        <asp:Literal ID="Literal2" runat="server" />
</p>
```

```csharp
protected void DropDownList1_SelectedIndexChanged(object sender, EventArgs e)
{
    Literal2.Text = DropDownList1.SelectedItem.Text;
}
```

<br/><br/>

ListBox kullanımı
```html
<asp:ListBox ID="ListBox1" runat="server"
             AutoPostBack="True" onselectedindexchanged="ListBox1_SelectedIndexChanged">

        <asp:ListItem>Web Programlama</asp:ListItem>
        <asp:ListItem>Bilgisayar Mimarisi</asp:ListItem>
        <asp:ListItem>Yazılım Mühendisliği</asp:ListItem>

</asp:ListBox>
<p>
        <asp:Literal ID="Literal3" runat="server" />
</p>
```

```csharp
protected void ListBox1_SelectedIndexChanged(object sender, EventArgs e)
{
   Literal3.Text = ListBox1.SelectedItem.Text;
}
```

<br/><br/>

DropDownList ile CheckBox kullanımı
```html
<asp:CheckBox ID="CheckBox1" runat="server"
              oncheckedchanged="CheckBox1_CheckedChanged" Text="c#" />
<p>
    <asp:CheckBox ID="CheckBox2" runat="server" Text="vb" />
</p>

<asp:DropDownList ID="DropDownList2" runat="server"
                  AutoPostBack="True" onselectedindexchanged="DropDownList2_SelectedIndexChanged">

       <asp:ListItem Value="0">item1</asp:ListItem>
       <asp:ListItem Value="1">item2</asp:ListItem>

</asp:DropDownList>
```

```csharp
protected void DropDownList2_SelectedIndexChanged(object sender, EventArgs e)
{
    if (Convert.ToInt32(DropDownList2.SelectedItem.Value) == 0)
    {
        CheckBox1.Checked = true;
        CheckBox2.Checked = false;
    }
    else if (Convert.ToInt32(DropDownList2.SelectedItem.Value) == 1)
    {
        CheckBox1.Checked = false;
        CheckBox2.Checked = true;
    }
}
```

</br></br>

CheckBoxList kullanımı
```html
<asp:CheckBoxList ID="CheckBoxList1" runat="server"
                  AutoPostBack="True" onselectedindexchanged="CheckBoxList1_SelectedIndexChanged">

        <asp:ListItem Value="1">Asp.</asp:ListItem>
        <asp:ListItem Value="2">Bilgisayar</asp:ListItem>

</asp:CheckBoxList>

<asp:Literal ID="Literal4"
             runat="server" />
```

```csharp
protected void CheckBoxList1_SelectedIndexChanged(object sender, EventArgs e)
{
    if (Convert.ToInt32(CheckBoxList1.SelectedValue) == 1)
    {
        CheckBoxList1.SelectedItem.Selected = false;
        Literal4.Text = CheckBoxList1.Items[0].Text.ToString() + "NET";
    }
    else if (Convert.ToInt32(CheckBoxList1.SelectedValue) == 2)
    {
        CheckBoxList1.SelectedItem.Selected = false;
        Literal4.Text = CheckBoxList1.Items[1].Text.ToString() + " Mühendisliği";
    }
}
```

</br></br>

RadioButton kullanımı
```html
<asp:Label ID="Label1" runat="server" Text="Cinsiyetiniz :" />

<asp:RadioButton ID="RadioButton1" runat="server" Text="Kadın" />
<asp:RadioButton ID="RadioButton2" runat="server" Text="Erkek" />

<p>
  <asp:Button ID="Button2" runat="server"
              onclick="Button2_Click" Text="Seçim" />
</p>

<asp:Literal ID="Literal5" runat="server" />
```

```csharp
protected void Button2_Click(object sender, EventArgs e)
{
     if (RadioButton1.Checked == true)
         Literal5.Text = "Cinsiyetiniz :" + RadioButton1.Text;
     else if (RadioButton2.Checked == true)
         Literal5.Text = "Cinsiyetiniz :" + RadioButton2.Text;

     RadioButton1.Checked = false;
     RadioButton2.Checked = false;
}
```

</br></br>

RadioButtonList kullanımı
```html
<asp:RadioButtonList ID="RadioButtonList1" runat="server"
                     AutoPostBack="True" onselectedindexchanged="RadioButtonList1_SelectedIndexChanged">

        <asp:ListItem>Galatasaray</asp:ListItem>
        <asp:ListItem>Fenerbahçe</asp:ListItem>
        <asp:ListItem>Beşiktaş</asp:ListItem>

</asp:RadioButtonList>

<asp:Literal ID="Literal6" runat="server"></asp:Literal>
```

```csharp
protected void RadioButtonList1_SelectedIndexChanged(object sender, EventArgs e)
{
    if (RadioButtonList1.SelectedIndex == 0)
        Literal6.Text = RadioButtonList1.SelectedValue + " 1905 yılında kuruldu";
    else if (RadioButtonList1.SelectedIndex == 1)
        Literal6.Text = RadioButtonList1.SelectedValue + " 1907 yılında kuruldu";
    else if (RadioButtonList1.SelectedIndex == 2)
        Literal6.Text = RadioButtonList1.SelectedValue + " 1903 yılında kuruldu";
}
```

</br></br>

Takvim kullanımı
```html
<asp:Calendar ID="Calendar1" runat="server" BackColor="White"
              BorderColor="White" BorderWidth="1px" Font-Names="Verdana"
              Font-Size="9pt" ForeColor="Black" Height="190px"
              NextPrevFormat="FullMonth" SelectedDate="03/13/2014 17:39:55" Width="350px"
              style="margin-left: 2px">

        <DayHeaderStyle Font-Bold="True" Font-Size="8pt" />
        <NextPrevStyle Font-Bold="True" Font-Size="8pt"
                       ForeColor="#333333" VerticalAlign="Bottom" />
        <OtherMonthDayStyle ForeColor="#999999" />
        <SelectedDayStyle BackColor="#333399" ForeColor="White" />
        <TitleStyle BackColor="White" BorderColor="Black" BorderWidth="4px"
                    Font-Bold="True" Font-Size="12pt" ForeColor="#333399" />
        <TodayDayStyle BackColor="#CCCCCC" />

</asp:Calendar>
```
