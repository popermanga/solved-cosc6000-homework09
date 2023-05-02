Download Link: https://assignmentchef.com/product/solved-cosc6000-homework09
<br>
Develop a class called <strong>BaseballPark</strong> that stores Baseball Parks data

Your class will have at least <strong><u>five member variables. </u>(<u>must be private) t</u>y<u>pe std::strin</u>g</strong> to represent the franchise.

<strong><u>t</u></strong><strong>y<u>pe std::strin</u>g</strong> to represent the name of stadium. <strong><u>t</u>y<u>pe std::strin</u>g</strong> to represent the name of city. <strong><u>t</u>y<u>pe int</u></strong> to represent the capacity.

<strong><u>t</u></strong><strong>y<u>pe USLen</u>g<u>th</u></strong> to represent the center field dimension.

You have developed <strong>USLength</strong> class in HW7.

The complete class will include all the following member functions:

a constructor to set a franchise, stadium, city, capacity and center field dimension as

<strong>BaseballPark park(franchise, stadium, city, capacity, centerField)</strong>; a default constructor (takes no input) that sets name=”NA”, and default number (maybe 0).

Mutators for each member variable.

Accessors for each member variable.

Add “<strong>const</strong>” modifier for <strong><u>member function that does not modif</u>y<u> member variables</u></strong>.

Develop C++ code to process following tasks:

Reads “<strong>MajorLeagueBallparks.csv</strong>” and store those in an array.

Download the file from <strong><u>here</u></strong>.

How to read CSV (Comma­Separated Values) file in C++? See below or see <strong><u>here</u></strong>

<strong><u>(http://www.cplusplus.com/forum/</u></strong><strong>g<u>eneral/13087/) </u></strong>.

Use your <strong>BaseballPark</strong> class to recored data.

Use <strong>std::vector</strong> container class to store all data in an array.

Your vector type must be like:

#include “USLength.h”




class BaseballPark{ public:

BaseballPark();

BaseballPark(std::string franchise,std::string stadium,std::string city,int capacity,USLength cente rField);




/// member/friend functions

private:     std::string franchise;     std::string stadium;     std::string city;     int capacity;

USLength centerField; // you may need your namespace

};




///

/// your code here

///

int main(int argc, const char * argv[]) {




// YOUR code here




std::ifstream infile;

infile.open(“MajorLeagueBallparks.csv”);// Path to the CSV file     if (infile.fail()){

std::cout &lt;&lt; “file not found
”;         return -1;

}

std::string franchise;     std::string stadium;     std::string city;     int capacity;     int yards;     int feet;

std::string entry;




std::string line;

while (std::getline(infile,line)){         std::stringstream ststrm(line);         std::getline(ststrm,franchise,’,’);         std::getline(ststrm,stadium,’,’);         std::getline(ststrm,city,’,’);         std::getline(ststrm,entry,’,’);         capacity = std::stoi(entry);         std::getline(ststrm,entry,’,’);         yards = std::stoi(entry);         std::getline(ststrm,entry);         feet = std::stoi(entry);




USLength centerField(yards,feet,0);//you might need namespace

BaseballPark bbpark(franchise,stadium,city,capacity,centerField);         // YOUR code here

Upload your USLength class files as well as your code if you make some changes onUSLength class.