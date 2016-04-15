## Overview
Given the below code:
* What potential problems do you see? 
* What might you cleanup / change / refactor?
* What other ways might the HTTP calls be made?


```C#
// Assume this code is in a web service and searchCountryID can come from anywhere
public string GetCountryData(int searchCountryID)
{
    string coStr = String.Empty;
    try
    {
        coStr = new MyApp.DataBase.Geo.CountryData().GetAllCountries()
            .Where(x => x.CountryId == searchCountryID).First().Abbreviation;
    }
    catch { }

    var url = "http://someplace.net/countries/?country=" + coStr;
    var req = (HttpWebRequest) WebRequest.Create(new Uri(url));

    HttpWebResponse res = null;
	string result = null;
	
    try
    {
        res = req.GetResponse() as HttpWebResponse;

        StreamReader reader = new StreamReader(res.GetResponseStream());
        result = reader.ReadToEnd();
        reader.Close();
        res.Close();
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.ToString());
    }
	
	return result;
}
```