# GifImage
Contains libraries to play GIFs in WinForms

# Usage

# C#

    public partial class Form1: Form
    {
        private GifImage gifImage = null;
        private string filePath = @"%GIF file path%";
     
        public Form1()
        {
            InitializeComponent();
            gifImage = new GifImage(filePath);
            gifImage.ReverseAtEnd = false;
        }

         private void button1_Click(object sender, EventArgs e)
        {
            timer1.Enabled = true;
        }
        
        private void timer1_Tick(object sender, EventArgs e)
        {
            pictureBox1.Image = gifImage.GetNextFrame();
        }
    }

# VB.NET

    Public Partial Class Form1
        Inherits Form

        Private gifImage As GifImage = Nothing
        Private filePath As String = "%GIF file path%"

        Public Sub New()
            InitializeComponent()
            Dim gifImage As New GifImage(filePath)
            gifImage.ReverseAtEnd = False
        End Sub

        Private Sub button1_Click(ByVal sender As Object, ByVal e As EventArgs)
            timer1.Enabled = True
        End Sub

        Private Sub timer1_Tick(ByVal sender As Object, ByVal e As EventArgs)
            pictureBox1.Image = gifImage.GetNextFrame()
        End Sub
    End Class
