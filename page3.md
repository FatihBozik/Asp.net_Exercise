#WebSite3

Asp.net Menü kullanımı

```html
<form id="form1" runat="server">
    <div>
        <asp:SiteMapPath ID="SiteMapPath1" runat="server" />
    </div>
    
    <asp:Menu ID="Menu1" runat="server" BackColor="#B5C7DE"
              DynamicHorizontalOffset="2" Font-Names="Verdana" Font-Size="0.8em"
              ForeColor="#284E98" StaticSubMenuIndent="10px">
        <DynamicHoverStyle BackColor="#284E98" ForeColor="White" />
        <DynamicMenuItemStyle HorizontalPadding="5px" VerticalPadding="2px" />
        <DynamicMenuStyle BackColor="#B5C7DE" />
        <DynamicSelectedStyle BackColor="#507CD1" />
        <Items>
            <asp:MenuItem NavigateUrl="~/Anasayfa.aspx" Text="Anasayfa" Value="Anasayfa">
                <asp:MenuItem NavigateUrl="~/Sayfa1.aspx" Text="Sayfa1" Value="Sayfa1">
                    <asp:MenuItem NavigateUrl="~/Sayfa2.aspx" Text="Sayfa2" Value="Sayfa2" />
                    <asp:MenuItem NavigateUrl="~/Sayfa3.aspx" Text="Sayfa3" Value="Sayfa3" />
                </asp:MenuItem>
                <asp:MenuItem NavigateUrl="~/Sayfa4.aspx" Text="Sayfa4" Value="Sayfa4" />
            </asp:MenuItem>
        </Items>
        <StaticHoverStyle BackColor="#284E98" ForeColor="White" />
        <StaticMenuItemStyle HorizontalPadding="5px" VerticalPadding="2px" />
        <StaticSelectedStyle BackColor="#507CD1" />
    </asp:Menu>
    </form>
```
