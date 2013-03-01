---
comments: true
date: 2011-04-19 22:22:00
layout: post
slug: ruby-visto-da-un-programmatore-c-pillole
title: Ruby visto da un programmatore C# (pillole)
wordpress_id: 7
categories:
- Ruby &amp; RubyOnRails
---

Come gia scritto in alcuni post precedenti, nell'ultimo anno mi sono interessato al linguaggio Ruby un po' per hobby e un po' per professione ci sto prendendo gusto. Volevo quindi raccontare in questo post e nei successivi quali sono le differenze rispetto a C# e mostrare alcune "stranezze" del linguaggio. Stranezze per chi e abituato a C#.




Ruby e un linguaggio ad oggetti come C# ma un po' piu ad oggetti rispetto a C#. In ruby tutto e un oggetto anche la definizione di una classe e un oggetto, anche nil (il null di C#) e un oggetto.




Inoltre, per la sua natura dinamica, un oggetto a differenza di C# puo cambiare nel tempo, ossia posso aggiungere e rimuovere metodi ad un oggetto.




Facciamo un esempio: se io ho una classe Money cosi definita:



    
    
    class Money
      def initialize(value)
        @value = value
      end  
      def value
        @value
      end
    end
    




L'istanza di questa classe rappresenta un importo in denaro. Sarebbe comodo ottenere un'istanza di Money in questo modo:



    
    
    money = 100.to_money
    




Dove 100 in ruby e un'istanza di Numeric (classe del "framework" ruby).  
Per farlo e necessario "aprire" la classe Numeric e aggiungere il metodo to_money in questo modo.



    
    
    class Numeric
      def to_money
        Money.new(self)
      end
    end
    




Dopo questa dichiarazione tutte le istanze di Numeric avranno un nuovo metodo to_money. La stessa cosa in C# si puo fare con gli extension methods, dall'esterno l'usabilita e simile ma converrete con me che in ruby e molto piu pulito e piu object oriented che in C#.
