# Java-CSV-Formulas

//Java: Create CSV file for Google Sheets only
//NOT for Excel



import java.io.FileWriter; 



public class CSVAekaterini {  
    public static void main(String args[]){    
         try{   
        

 
 
           //create csv file products
           FileWriter fw=new FileWriter("/myfiles/products.csv");
           
           //enter dataset in file
           //4 columns 
           fw.write("id, product, cost, quantity\n");
           fw.write("101, mascara, 9.50, 280\n");
           fw.write("102, blush, 5.50, 560\n");
           fw.write("103, lipgloss, 11.80, 330\n");
           fw.write("104, nail polish,18.00, 106\n");
           fw.write("105, blush, 5.00, 98\n");
           fw.write("106, perfume, 15.00, 220\n");
           fw.write("107, mascara, 12.50, 430\n");
           fw.write("                        \n");
           
           //Statistical Formulas
           fw.write("Statistical Formulas\n");
           fw.write("Sum quantity,  ,=sum(d2:d8)\n");
           fw.write("Average cost,  ,=average(c2:c8)\n");
           fw.write("Lowest cost,  ,=min(c2:c8)\n");
           fw.write("Highest cost,  ,=max(c2:c8)\n");
           fw.write("Count records, ,=count(a2:a8)\n");
           fw.write("Sum quantity of blush,   ,\"=sumifs(D2:D8,B2:B8,\"\"blush\"\")\"\r\n");
           fw.write("Average quantity of mascara,  , \"=averageifs(D2:D8,B2:B8,\"\"mascara\"\")\"\r\n");
           fw.write("Lowest cost of mascara,   ,\"=minifs(D2:D8,B2:B8,\"\"mascara\"\")\"\r\n");
           fw.write("Highest cost of mascara,   ,\"=maxifs(D2:D8,B2:B8,\"\"mascara\"\")\"\r\n");
        
           //Equavalent to basic SQL
           fw.write("Find product with id 103,  ,\"=vlookup(103, A2:B8, 2, \"\"false\"\")\"\r\n");
           fw.write("Find quantity of blush,    ,\"=vlookup(\"\"blush\"\", b2:c8, 2, \"\"false\"\")\"\r\n");
           
           
           fw.close();
           
          }catch(Exception e){System.out.println(e);}    
          System.out.println("Success file created!");    
     }    
}
