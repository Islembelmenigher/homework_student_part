#include <iostream>
#include <string>
#include <vector>
using namespace std;
class Student {
public:
    std::string name;
    std::string surname;
    int album_num;
    std::vector<float> grades;

public:
    void set_name(std::string new_name) {
        name = new_name;
    }

    void set_surname(std::string new_surname) {
        surname = new_surname;
    }

    void set_album_num(int new_album_num) {
        if (new_album_num < 10000 || new_album_num > 999999) {
            std::cout << "Error: Invalid album number.\n";
            return;
        }
        album_num = new_album_num;
    }

    void add_grade(float new_grade) {
        if (new_grade < 2.0 || new_grade > 5.0) {
            std::cout << "Error: Invalid grade.\n";
            return;
        }
        grades.push_back(new_grade);
    }

    float calculate_mean_grade() {
        if (grades.size() == 0) {
            std::cout << "Error: No grades.\n";
            return 0.0;
        }
        float sum = 0.0;
        for (int i = 0; i < grades.size(); i++) {
            sum += grades[i];
        }
        return sum / grades.size();
    }

    bool check_if_passed_semester() {
        int num_twos = 0;
        for (int i = 0; i < grades.size(); i++) {
            if (grades[i] == 2.0) {
                num_twos++;
            }
        }
        return num_twos <= 1;
    }

    void display_summary() {
        std::cout << "Name: " << name << "\n";
        std::cout << "Surname: " << surname << "\n";
        std::cout << "Album num: " << album_num << "\n";
        std::cout << "Grades: ";
        for (int i = 0; i < grades.size(); i++) {
            std::cout << grades[i] << " ";
        }
        std::cout << "\nMean grade: " << calculate_mean_grade() << "\n";
        std::cout << "Passed semester: " << (check_if_passed_semester() ? "Yes" : "No") << "\n";
    }
};

int main() {
    Student islem;
    islem.set_name("islem");
    islem.set_surname("belmenigher");
    islem.set_album_num(156722);
    islem.add_grade(4.5);
    islem.add_grade(2.0);
    islem.add_grade(4.0);
    islem.display_summary();
    return 0;
}
