 protected void Manpower_calculate()
        {
            string male = ((TextBox)Register_Record.Rows[0].FindControl("Conservancy_Male")).Text;
            string female = ((TextBox)Register_Record.Rows[0].FindControl("Conservancy_Female")).Text;
            string d2d = ((TextBox)Register_Record.Rows[0].FindControl("D2D")).Text;
            string bush = ((TextBox)Register_Record.Rows[0].FindControl("Bush_Cutting")).Text;
            string sup = ((TextBox)Register_Record.Rows[0].FindControl("Sup")).Text;
            string dri = ((TextBox)Register_Record.Rows[0].FindControl("Dri")).Text;

            if (male != "" && female == "" && d2d == "" && bush == "" && sup == "" && dri == "")
            {
                Double result = Convert.ToDouble(male);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("Conservancy_Female")).Focus();
            }
            if (male != "" && female != "" && d2d == "" && bush == "" && sup == "" && dri == "")
            {
                Double result = Convert.ToDouble(male) + Convert.ToDouble(female);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("D2D")).Focus();
            }
            if (male != "" && female != "" && d2d != "" && bush == "" && sup == "" && dri == "")
            {
                Double result = Convert.ToDouble(male) + Convert.ToDouble(female) + Convert.ToDouble(d2d);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("Bush_Cutting")).Focus();
            }
            if (male != "" && female != "" && d2d != "" && bush != "" && sup == "" && dri == "")
            {
                Double result = Convert.ToDouble(male) + Convert.ToDouble(female) + Convert.ToDouble(d2d) + Convert.ToDouble(bush);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("Sup")).Focus();
            }
            if (male != "" && female != "" && d2d != "" && bush != "" && sup != "" && dri == "")
            {
                Double result = Convert.ToDouble(male) + Convert.ToDouble(female) + Convert.ToDouble(d2d) + Convert.ToDouble(bush) + Convert.ToDouble(sup);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("Dri")).Focus();
            }
            if (male != "" && female != "" && d2d != "" && bush != "" && sup != "" && dri != "")
            {
                Double result = Convert.ToDouble(male) + Convert.ToDouble(female) + Convert.ToDouble(d2d) + Convert.ToDouble(bush) + Convert.ToDouble(sup) + Convert.ToDouble(dri);
                ((TextBox)Register_Record.Rows[0].FindControl("Stnd_Manpower")).Text = Convert.ToString(result);
                ((TextBox)Register_Record.Rows[0].FindControl("Rickshaw")).Focus();
            }
        }
