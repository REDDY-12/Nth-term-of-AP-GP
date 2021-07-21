# Nth-term-of-AP-GP
# This code gives us the nth term of Arithmetic Progression(AP) and Geometric Progression(GP) when the required fiels are entered..
# Code starts here...
def arithmetic_progression(ap_series, nth_term_ap):
    first_term_ap = ap_series[0]
    second_term_ap = ap_series[1]
    difference = second_term_ap - first_term_ap
    nth_value = first_term_ap + (nth_term_ap - 1) * difference
    print("The nth term of given AP series is: ", nth_value)
    exit()


def geometric_progression(gp_series, nth_term_gp):
    first_term_gp = gp_series[0]
    second_term_gp = gp_series[1]
    common_ratio = second_term_gp / first_term_gp
    nth_value = first_term_gp * pow(common_ratio, nth_term_gp - 1)
    print("The nth term of given AP series is: ", nth_value)
    exit()

check = input("Which series you want to check...? : \n 1) Arithmetic Progression\n 2) Geometric Progression\n 
              "Press 1 for AP or 2 for GP \nType your choice here:  ")
if check == "1":
    ap_series = list(map(int, input("Enter the AP series: ").split(",")))
    nth_term_ap = int(input("Enter the nth term of AP: "))
    print(arithmetic_progression(ap_series, nth_term_ap))
elif check == "2":
    gp_series = list(map(int, input("Enter the GP series: ").split(",")))
    nth_term_gp = int(input("Enter the nth term of GP: "))
    print(geometric_progression(gp_series, nth_term_gp))
else:
    print("Sorry wrong input, choose correctly...")
