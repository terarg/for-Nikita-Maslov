# for-Nikita-Maslov

sing System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
using System.Drawing.Drawing2D;

namespace WindowsFormsApplication3
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        protected override void OnPaint(PaintEventArgs e)
        {
            Graphics g = e.Graphics;
            SolidBrush bus= new SolidBrush(Color.Yellow);
            Pen outline = new Pen(Color.Black);
            SolidBrush will = new SolidBrush(Color.Gray);
            SolidBrush willOut = new SolidBrush(Color.Black);
            SolidBrush window = new SolidBrush(Color.White);
            SolidBrush door = new SolidBrush(Color.PaleGoldenrod);
            SolidBrush light = new SolidBrush(Color.Peru);
            SolidBrush lighting = new SolidBrush(Color.Gold);
            SolidBrush road = new SolidBrush(Color.DarkGray);
            SolidBrush razmetka = new SolidBrush(Color.White);
            SolidBrush sky = new SolidBrush(Color.LightCyan);
            SolidBrush driver = new SolidBrush(Color.SaddleBrown);

            g.FillRectangle(sky, 0, 0, 800, 600);

            g.FillRectangle(road, 0, 270, 800, 320);
            for (int i = 0; i < 800; i+=100)
                g.FillRectangle(razmetka, 0 + i, 353, 80, 30);

            g.DrawRectangle(outline, 50, 50, 500, 250);
            g.FillRectangle(bus, 51, 51, 499, 249);

            g.FillEllipse(willOut, 70, 300, 60, 60);
            g.FillEllipse(willOut, 450, 300, 60, 60);
            g.FillEllipse(will, 80, 310, 40, 40);
            g.FillEllipse(will, 460, 310, 40, 40);

            g.FillRectangle(window, 100, 100, 100, 80);
            g.FillRectangle(window, 210, 100, 100, 80);
            g.FillRectangle(window, 450, 80, 100, 120);

            g.FillEllipse(driver, 470, 140, 40, 40);
            g.FillRectangle(driver, 485, 160, 10, 40);

            g.FillEllipse(driver, 120, 140, 40, 40);
            g.FillEllipse(driver, 230, 140, 40, 40);

            g.DrawRectangle(outline, 320, 100, 100, 190);
            g.FillRectangle(door, 321, 101, 99, 189);

            g.FillPie(lighting, 500, 220, 100, 100, -70, 137);
            g.FillPie(light, 520, 250, 40, 40, -70, 137);

           
        }
    }
}
