from constants import PLAYERS,TEAMS
import copy
app_constants = copy.deepcopy(PLAYERS)
    
def clean_data(app_constants):
   for app_players in app_constants:
       app_players['height'] = int(app_players['height'].split(' inches'))
       if app_players['experience'] == "YES":
           app_players['experience'] = True
       else:
           app_players['experience'] = False
       
def main():
    print('BASKETBALL TEAM STATS TOOL\n\n')
    print('----MENU----\n\n')
    print('  Here are your choices')
    print('    1) Display Team Stats')
    print('    2) Quit')
    selection1 = input('Enter an option >')
   
    if selection1 == '1':
        print('\n1) Panthers\n')
        print('2) Bandits\n')
        print('3) Warriors\n')
        selection2 = int(input('Enter an option >'))
        valid_input = [1, 2, 3]
        while selection2 not in valid_input:
            selection2 = int(input('Enter an option >'))
    else:
        print('Come back to check out the latest stats!')
        return 
    
    team_selection = TEAMS[selection2-1]
    print('\nTeam: ', team_selection)
    print('--------------------')
    clean_data(app_constants)
    
    
    def balance_teams(app_constants):
        player_list = app_constants[selection2::len(TEAMS)]
        name_list = [app_players['name'] for app_players in player_list]
        print('Total players: ',len(player_list), '\n')
        print(', '.join(name_list))
    balance_teams(app_constants)
    end_app = input('\nPress Enter to continue: ')
    if end_app == '':
        main()
    else:
        print("See you next time")
        return
    
        

if __name__ == '__main__':
    main()
