using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Xml.Linq;

namespace xmllinqdelete
{
    class Program
    {
        static void Main(string[] args)
        {
          
                String path = "c:/users/mslceltp1045/documents/visual studio 2015/Projects/xmllinqdelete/xmllinqdelete/xmldelete/XMLFile1.xml";
                XDocument xdoc = XDocument.Load(path);
                var product = xdoc.Descendants("product").Single(p => p.Attribute("id").Value.Equals("p04"));

                product.Remove();
                xdoc.Save("path");
                Console.Write(xdoc);
            
           
            Console.ReadLine();


        }

    }
}
