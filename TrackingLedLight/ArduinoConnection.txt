import pyfirmata

comPort = 'COM3'
board = pyfirmata.Arduino(comPort)
led_1 = board.get_pin('d:13:o')
led_2 = board.get_pin('d:12:o')
led_3 = board.get_pin('d:11:o')
led_4 = board.get_pin('d:10:o')
led_5 = board.get_pin('d:9:o')
class ValueOfLight:
    def ledLight(val):
        if val == 1:
            led_1.write(1)
            led_2.write(0)
            led_3.write(0)
            led_4.write(0)
            led_5.write(0)
        elif val == 2:
            led_1.write(1)
            led_2.write(1)
            led_3.write(0)
            led_4.write(0)
            led_5.write(0)
        elif val == 3:
            led_1.write(1)
            led_2.write(1)
            led_3.write(1)
            led_4.write(0)
            led_5.write(0)
        elif val == 4:
            led_1.write(1)
            led_2.write(1)
            led_3.write(1)
            led_4.write(1)
            led_5.write(0)
        elif val == 5:
            led_1.write(1)
            led_2.write(1)
            led_3.write(1)
            led_4.write(1)
            led_5.write(1)
        else:
            led_1.write(0)
            led_2.write(0)
            led_3.write(0)
            led_4.write(0)
            led_5.write(0)
