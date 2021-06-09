# mailhydra


### Coding responsive colums with HTML tables
[References:Developing HTML Emails Using “Ghost Tables”](https://webdesign.tutsplus.com/tutorials/html-email-using-ghost-tables--cms-32551)

![Two Columns Example](https://www.mailhydra.com/img/two-columns-no-ghost-table-example.png)
### Columns (no ghost tables)

```html
<tr>
    <td>


        <table width=100%>
            <tr>
                <td class="two-columns" valign=top style="font-size:0;">


                    <table style="max-width: 250; vertical-align: top; display: inline-block;">
                        <tr>
                            <td>
                                <p>Content goes here. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam, nemo.</p>
                            </td>
                        </tr>
                    </table>

                    <table style="max-width: 250; vertical-align: top;width: 100%; display: inline-block;">
                        <tr>
                            <td>
                                <p>Content goes here. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam, nemo.</p>
                            </td>
                        </tr>
                    </table>


                </td>
            </tr>
        </table>

    </td>
</tr>
```
### Columns with included ghost tables for Outlook support 
```HTML
<tr>
    <td>


        <table width=100%>
            <tr>
                <td class="two-columns" valign=top style="font-size:0;">
                    <!--[if (gte mso 9)|(IE)]>
                    <table width="100%" style="border-spacing: 0;" role="presentation">
                        <tr>
                       
                        <td width="300" valign="top" style="padding: 0;">
                        <![endif]-->

                    <table style="max-width: 250; vertical-align: top; display: inline-block;">
                        <tr>
                            <td>
                                <p>Content goes here. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam,
                                    nemo.</p>
                            </td>
                        </tr>
                    </table>

                      <!--[if (gte mso 9)|(IE)]>
                      </td>
                      <td width="300" valign="top" style="padding: 0;">
                      <![endif]-->
                    


                    <table style="max-width: 250; vertical-align: top;width: 100%; display: inline-block;">
                        <tr>
                            <td>
                                <p>Content goes here. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam,
                                    nemo.</p>
                            </td>
                        </tr>
                    </table>
                      <!--[if (gte mso 9)|(IE)]>
                        </td>
                        </tr>
                   </table>
                   <![endif]-->


                </td>
            </tr>
        </table>

    </td>
</tr>
```
