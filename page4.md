#Website4

Web.sitemap
```html
<?xml version="1.0" encoding="utf-8" ?>
<siteMap xmlns="http://schemas.microsoft.com/AspNet/SiteMap-File-1.0" >
    <siteMapNode url="Anasayfa.aspx" title="anasayfa"  description="anasayfa">
        <siteMapNode url="Ürünler.aspx" title="ürünler"  description="ürünler" >
            <siteMapNode url="Bilgisayar.aspx" title="Bilgisayar"  description="Bilgisayar" />
            <siteMapNode url="Telefon.aspx" title="Telefon"  description="Telefon" />
        </siteMapNode>

        <siteMapNode url="İletişim.aspx" title="İletişim"  description="İletişim" />
    </siteMapNode>
</siteMap>


```
<br /> <br />

Anasayfa.aspx
```html
<asp:Menu ID="Menu1" runat="server" DataSourceID="SiteMapDataSource1" />
<asp:SiteMapDataSource ID="SiteMapDataSource1" runat="server"/>
```
