"""
Test para anotar en juego de tenis,
al metodo entran los parametros de
-el jugador que anota
-el puntaje actual del jugador 1
-el puntaje actual del jugador 2

...para el adv se utiliza el 41...


>>> anotar(1,0,0)
'15-0'

>>> anotar (2,0,0)
'0-15'

>>> anotar(1,15,0)
'30-0'

>>> anotar(2,0,15)
'0-30'

>>> anotar(1,15,15)
'30-15'

>>> anotar (2,15,15)
'15-30'

>>> anotar(1,30,30)
'40-30'

>>> anotar (2,30,30)
'30-40'

>>> anotar(1,30,15)
'40-15'

>>> anotar (2,15,30)
'15-40'

>>> anotar(1,40,15)
'juego player 1'

>>> anotar (2,15,40)
'juego player 2'

>>> anotar(1,40,30)
'juego player 1'

>>> anotar (2,30,40)
'juego player 2'

>>> anotar(1,30,40)
'deuce'

>>> anotar(2,40,30)
'deuce'

>>> anotar(1,40,40)
'Adv-40'

>>> anotar(2,40,40)
'40-Adv'

>>> anotar(1,41,40)
'juego player 1'

>>> anotar(2,40,41)
'juego player 2'

>>> anotar(1,40,41)
'deuce'

>>> anotar(2,41,40)
'deuce'


"""


def anotar(player, actual1, actual2):
    if player == 1:
        if actual1 == 0:
            return '15-' + str(actual2)
        elif actual1 == 15:
            return '30-' + str(actual2)
        elif actual1 == 30:
            actual1 = 40
            if chek_duece(actual1, actual2) == 1:
                return 'deuce'
            else:
                return '40-' + str(actual2)
        elif actual1 == 40 and actual2 < 40:
            return 'juego player 1'
        elif actual1 == 40 and actual2 == 40:
            return 'Adv-40'
        elif actual1 == 41:
            return 'juego player 1'
        elif actual2 == 41 and actual1 == 40:
            return 'deuce'
    else:
        if actual2 == 0:
            return str(actual1) + '-15'
        elif actual2 == 15:
            return str(actual1) + '-30'
        elif actual2 == 30:
            actual2 = 40
            if chek_duece(actual1, actual2) == 1:
                return 'deuce'
            else:
                return str(actual1) + '-40'
        elif actual2 == 40 and actual1 < 40:
            return 'juego player 2'
        elif actual2 == 40 and actual1 == 40:
            return '40-Adv'
        elif actual2 == 41:
            return 'juego player 2'
        elif actual1 == 41 and actual2 == 40:
            return 'deuce'


def chek_duece(actual1, actual2):
    if actual1 == actual2:
        return 1
    else:
        return 0


if __name__ == '__main__':
    import doctest
    doctest.testmod()
