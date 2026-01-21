protected void gvManpower_RowDataBound(object sender, GridViewRowEventArgs e)
{
    if (e.Row.RowType == DataControlRowType.DataRow)
    {
        decimal male = ToDecimal(DataBinder.Eval(e.Row.DataItem, "Male"));
        decimal female = ToDecimal(DataBinder.Eval(e.Row.DataItem, "Female"));
        decimal bush = ToDecimal(DataBinder.Eval(e.Row.DataItem, "Bush"));
        decimal sup = ToDecimal(DataBinder.Eval(e.Row.DataItem, "Supervisor"));
        decimal driver = ToDecimal(DataBinder.Eval(e.Row.DataItem, "Driver"));

        decimal rowTotal = male + female + bush + sup + driver;

        ((Label)e.Row.FindControl("lblRowTotal")).Text = rowTotal.ToString("0.00");

        gMale += male;
        gFemale += female;
        gBush += bush;
        gSup += sup;
        gDriver += driver;
        gGrand += rowTotal;
    }

    if (e.Row.RowType == DataControlRowType.Footer)
    {
        ((Label)e.Row.FindControl("lblMaleTotal")).Text = gMale.ToString("0.00");
        ((Label)e.Row.FindControl("lblFemaleTotal")).Text = gFemale.ToString("0.00");
        ((Label)e.Row.FindControl("lblBushTotal")).Text = gBush.ToString("0.00");
        ((Label)e.Row.FindControl("lblSupervisorTotal")).Text = gSup.ToString("0.00");
        ((Label)e.Row.FindContro
                    <EditRowStyle BackColor="#999999" />
                    <FooterStyle BackColor="#5D7B9D" ForeColor="White" Font-Bold="True" />
                    <HeaderStyle BackColor="#666666" Font-Bold="True" ForeColor="White" Height="1%" />
                    <PagerSettings Mode="Numeric"/>
                    <PagerStyle BackColor="#284775" ForeColor="White" HorizontalAlign="Center" Font-Bold="True" CssClass="pager1" />
                    <PagerStyle BackColor="#284775" ForeColor="White" HorizontalAlign="Center" />
                    <RowStyle BackColor="#F7F6F3" ForeColor="#333333" />
                    <SelectedRowStyle BackColor="#E2DED6" Font-Bold="False" ForeColor="#333333" />
                    <SortedAscendingCellStyle BackColor="#E9E7E2" />
                    <SortedAscendingHeaderStyle BackColor="#506C8C" />
                    <SortedDescendingCellStyle BackColor="#FFFDF8" />
                    <SortedDescendingHeaderStyle BackColor="#6F8DAE" />
                 </asp:GridView>
                      </div>
