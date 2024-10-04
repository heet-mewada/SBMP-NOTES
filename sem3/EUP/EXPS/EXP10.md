using System;

using System.Collections.Generic;

using System.ComponentModel;

using System.Data;

using System.Drawing;

using System.Linq;

using System.Text;

using System.Threading.Tasks;

using System.Windows.Forms;

using System.Data.SqlClient;

namespace EXP10

{

public partial class Form1 : Form

{

SqlConnection conn;

string query;

SqlDataAdapter sda;

DataTable dt;

string stname, capname;

DataRow row;

public Form1()

{

InitializeComponent();

conn = new SqlConnection(@"Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=C:\Users\SBMPC.student\source\repos\het\EXP10\Database1.mdf;Integrated Security=True");

query = "select state from city";

conn.Open();

sda = new SqlDataAdapter(query, conn);

dt = new DataTable();

sda.Fill(dt);

for (int i = 0; i < dt.Rows.Count; i++)

{

row = dt.Rows[i];

stname = row[0].ToString();

comboBox1.Items.Add(stname);

}

this.FormClosing += new FormClosingEventHandler(this.MyForm_FormClosing);

}

private void Form1_Load(object sender, EventArgs e)

{

}

private void button1_Click(object sender, EventArgs e)

{

stname = comboBox1.SelectedItem.ToString();

query = "select capital from city where state='" + stname + "'";

MessageBox.Show(query);

sda = new SqlDataAdapter(query, conn);

dt = new DataTable();

sda.Fill(dt);

row = dt.Rows[0];

capname = row[0].ToString();

textBox1.Text = capname;

}

private void button2_Click(object sender, EventArgs e)

{

Form2 frm2=new Form2();

frm2.Show();

}

private void label2_Click(object sender, EventArgs e)

{

}

private void MyForm_FormClosing(object sender, FormClosingEventArgs e)

{

if (MessageBox.Show("Do you want to close the form ?", "STATE CAPITAL", MessageBoxButtons.YesNo) == DialogResult.Yes)

{

MessageBox.Show("Closing connection");

conn.Close();

}

else if (MessageBox.Show("Do you want to close the form ?", "STATE CAPITAL", MessageBoxButtons.YesNo) == DialogResult.No)

{

e.Cancel = true;

}

}

}

}

using System;

using System.Collections.Generic;

using System.ComponentModel;

using System.Data;

using System.Data.SqlClient;

using System.Drawing;

using System.Linq;

using System.Text;

using System.Threading.Tasks;

using System.Windows.Forms;

using System.Data.SqlClient;

using static System.Windows.Forms.VisualStyles.VisualStyleElement;

namespace EXP10

{

public partial class Form2 : Form

{

SqlConnection conn;

string query;

SqlDataAdapter sda;

DataTable dt;

string stname, capname;

DataRow row;

public Form2()

{

InitializeComponent();

conn = new SqlConnection(@"Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=C:\Users\SBMPC.student\source\repos\het\EXP10\Database1.mdf;Integrated Security=True");

query = "select sport from sport";

conn.Open();

sda = new SqlDataAdapter(query,conn);

dt = new DataTable();

sda.Fill(dt);

for (int i = 0; i < dt.Rows.Count; i++)

{

row = dt.Rows[i];

stname = row[0].ToString();

listBox1.Items.Add(stname);

}

this.FormClosing += new FormClosingEventHandler(this.MyForm_FormClosing);

}

private void button1_Click(object sender, EventArgs e)

{

stname = listBox1.SelectedItem.ToString();

dt = new DataTable();

sda.Fill(dt);

textBox1.Text = stname;

}

private void Form2_Load(object sender, EventArgs e)

{

}

private void label2_Click(object sender, EventArgs e)

{

}

private void label1_Click(object sender, EventArgs e)

{

}

private void MyForm_FormClosing(object sender, FormClosingEventArgs e)

{

if (MessageBox.Show("Do you want to close the form ?", "STATE CAPITAL", MessageBoxButtons.YesNo) == DialogResult.Yes)

{

MessageBox.Show("Closing connection");

conn.Close();

}

else if (MessageBox.Show("Do you want to close the form ?", "STATE CAPITAL", MessageBoxButtons.YesNo) == DialogResult.No)

{

e.Cancel = true;

}

}

}

}