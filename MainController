using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using System.Linq;

public class MainController : MonoBehaviour {

    int a;
    int b;
    int c;

    public GameObject winObj;
    public GameObject blankWin;
    

    [SerializeField]
    private Text text1;
    [SerializeField]
    private Text text2;
    [SerializeField]
    private Text text3;
    [SerializeField]
    private Text text4;
    [SerializeField]
    private Text text5;

    [SerializeField]
    private Text botonText1;
    [SerializeField]
    private Text botonText2;
    [SerializeField]
    private Text botonText3;

    int bt1;
    int bt2;
    int bt3;

    bool IsEmpty1 = true;
    bool IsEmpty2 = true;
    bool IsEmpty3 = true;

    //Animation
    [SerializeField]
    private GameObject anim ;
    [SerializeField]
    private GameObject wellDoneAnimation;
    [SerializeField]
    private float timeAnimation = 1.8f;
    
    //List
    public List<int> resultados = new List<int>();
    //CountOperationDone
    public int countOperationsDone ;


    void Start()
    {
        
        countOperationsDone = 1;
        RandomNumbers(a, b);
        text1.text = a.ToString() ;
        Debug.Log("a" + a);
        text2.text = "+";
        text3.text = b.ToString();
        Debug.Log("b" + b);
        text4.text = "=";
        text5.text = "?";

        
        c = a + b;
        RandomNumberButton(bt1, bt2, bt3);
    
        resultados.Add(bt1);
        resultados.Add(bt2);
        resultados.Add(bt3);


       

    }

    private void Update()
    {
        AssignColorToNumbers();
        IsCompleteTheGame();
        AssignNumbers();

    }

    void AssignNumbers()
    {
        int randomIndex = Random.Range(0, resultados.Count);
        if (IsEmpty1 == true)
        {
            botonText1.text = resultados[randomIndex].ToString();
            resultados.RemoveAt(randomIndex);
            IsEmpty1 = false;
        }
        if (IsEmpty2 == true)
        {
            botonText2.text = resultados[randomIndex].ToString();
            resultados.RemoveAt(randomIndex);
            IsEmpty2 = false;
        }
        if (IsEmpty3 == true)
        {
            botonText3.text = resultados[randomIndex].ToString();
            resultados.RemoveAt(randomIndex);
            IsEmpty3 = false;
        }
    }

    



    void RandomNumbers(int a, int b)
    {
         a = Random.Range(0, 9);
         b = Random.Range(0, 9);
        this.a = a;
        this.b = b;

    }

    void RandomNumberButton(int bt1, int bt2, int bt3)
    {
        
        bt1 = Random.Range(0, 20);
        bt2 = Random.Range(0, 20);
        bt3 = c;
        
        if(bt1 != bt2 && bt1 != bt3)
        {
            this.bt1 = bt1;
        }
        else
        {
            bt1 = Random.Range(0, 20);
        }
        if(bt2 != bt3 && bt2 != bt3)
        {
            this.bt2 = bt2;
        }
        else
        {
            bt2 = Random.Range(0, 20);
        }
        
        this.bt3 = bt3;
       
    }

    void IsCompleteTheGame()
    {
        if (countOperationsDone == 0)
        {
           Invoke("WaitAfterPerfectAnimation", 2);


        }
    }

    public void CheckBotonOne()
    {


       if(botonText1.text == c.ToString())
        {
            Debug.Log("WIN");
            text1.text = a.ToString();
            Debug.Log("a" + a);
            text2.text = "+";
            text3.text = b.ToString();
            Debug.Log("b" + b);
            text4.text = "=";
            text5.text = c.ToString();
            WellDoneAnimation();
            Invoke("ResetOperation", timeAnimation);
            countOperationsDone = countOperationsDone - 1;
            
           


        }
        else
        {
            Debug.Log("TRY AGAIN");
            TryAgainAnimation();
        }


    }
    public void CheckBotonTwo()
    {
        if (botonText2.text == c.ToString())
        {
            Debug.Log("WIN");
            text1.text = a.ToString();
            Debug.Log("a" + a);
            text2.text = "+";
            text3.text = b.ToString();
            Debug.Log("b" + b);
            text4.text = "=";
            text5.text = c.ToString();
            WellDoneAnimation();
            Invoke("ResetOperation", timeAnimation);
            countOperationsDone = countOperationsDone - 1;
           
        }
        else
        {
            Debug.Log("TRY AGAIN");
            TryAgainAnimation();
        }


    }
    public void CheckBotonThree()
    {
        if (botonText3.text == c.ToString())
        {
            Debug.Log("WIN");
            text1.text = a.ToString();
            Debug.Log("a" + a);
            text2.text = "+";
            text3.text = b.ToString();
            Debug.Log("b" + b);
            text4.text = "=";
            text5.text = c.ToString();
            WellDoneAnimation();
            Invoke("ResetOperation", timeAnimation);
            countOperationsDone = countOperationsDone - 1;
           


        }
        else
        {
            Debug.Log("TRY AGAIN");
            TryAgainAnimation();
        }


    }



    //Animation


    void TryAgainAnimation()
    {
        anim.SetActive(true);
        Invoke("TimeToCutOut", timeAnimation);
    }

    void WellDoneAnimation()
    {
        wellDoneAnimation.SetActive(true);
        Invoke("TimeToCutOut", timeAnimation);
    }

    void WaitAfterPerfectAnimation()
    {
        blankWin.SetActive(true);
        winObj.SetActive(true);
    }
    void TimeToCutOut()
    {
        anim.SetActive(false);
        wellDoneAnimation.SetActive(false);
       
    }


    //Reset Operation

    void ResetOperation()
    {
        
        
        a = 0;
        b = 0;
        c = 0;

        bt1 = 0;
        bt2 = 0;
        bt3 = 0;

        text1.text = null;
        text2.text = null;
        text3.text = null;
        text4.text = null;
        text5.text = null;

        botonText1.text = null;
        botonText2.text = null;
        botonText3.text = null;

        IsEmpty1 = true;
        IsEmpty2 = true;
        IsEmpty3 = true;

        RandomNumbers(a, b);

        text1.text = a.ToString();
        Debug.Log("a" + a);
        text2.text = "+";
        text3.text = b.ToString();
        Debug.Log("b" + b);
        text4.text = "=";
        text5.text = "?";

        c = a + b;

        RandomNumberButton(bt1, bt2, bt3);

        resultados.Add(bt1);
        resultados.Add(bt2);
        resultados.Add(bt3);
    }

    void AssignColorToNumbers()
    {
        if (a == 0)
        {
            text1.color = Color.green;
        }
        if (a == 1)
        {
            text1.color = Color.red;
        }
        if (a == 2)
        {
            text1.color = Color.blue;
        }
        if (a == 3)
        {
            text1.color = Color.magenta;
        }
        if (a == 4)
        {
            text1.color = Color.yellow;
        }
        if (a == 5)
        {
            text1.color = Color.cyan;
        }
        if (a == 6)
        {
            text1.color = Color.red;
        }
        if (a == 7)
        {
            text1.color = Color.green;
        }
        if (a == 8)
        {
            text1.color = Color.blue;
        }
        if (a == 9)
        {
            text1.color = Color.magenta;
        }

        if (b == 0)
        {
            text3.color = Color.green;
        }
        if (b == 1)
        {
            text3.color = Color.red;
        }
        if (b == 2)
        {
            text3.color = Color.blue;
        }
        if (b == 3)
        {
            text3.color = Color.magenta;
        }
        if (b == 4)
        {
            text3.color = Color.yellow;
        }
        if (b == 5)
        {
            text3.color = Color.cyan;
        }
        if (b == 6)
        {
            text3.color = Color.red;
        }
        if (b == 7)
        {
            text3.color = Color.green;
        }
        if (b == 8)
        {
            text3.color = Color.blue;
        }
        if (b == 9)
        {
            text3.color = Color.magenta;
        }

        text2.color = Color.gray;
        text4.color = Color.gray;
        text5.color = Color.black;
    }
}
