Numbers
========

ChangingDecimal
*****************
.. autoclass:: manimlib.animation.numbers.ChangingDecimal
    :members:
    
.. manim-example:: ChangingDecimalExample
  :media: ../_static/mk/ChangingDecimalExample.mp4

  class ChangingDecimalExample(Scene):
      def construct(self):
          number = DecimalNumber(0).scale(2)
          def update_func(t):
              return t * 10
          self.add(number)
          self.wait()
          self.play(ChangingDecimal(number, update_func), run_time=3)
          self.wait()

    
ChangeDecimalToValue
**********************
.. autoclass:: manimlib.animation.numbers.ChangeDecimalToValue
    :members:
    
.. manim-example:: ChangeDecimalToValueExample
  :media: ../_static/mk/ChangeDecimalToValueExample.mp4

  class ChangeDecimalToValueExample(Scene):
      def construct(self):
          number = DecimalNumber(0).scale(2)
          self.add(number)
          self.wait()
          self.play(ChangeDecimalToValue(number, 20), run_time=3)
          self.wait()
