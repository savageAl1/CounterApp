# CounterApp
CounterApp

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val btnClickMe = findViewById<Button>(R.id.button1)
        val tvMytextview = findViewById<TextView>(R.id.textView)
        val btn2Clickme = findViewById<Button>(R.id.button2)
        val tvMySave = findViewById<TextView>(R.id.textView2)
        val btn3Clickme= findViewById<Button>(R.id.button3)
        var timesClicked = 0

        btnClickMe.setOnClickListener {
            timesClicked = timesClicked + 1
            tvMytextview.text = timesClicked.toString()
        }


        btn2Clickme.setOnClickListener {
            timesClicked = 0
            tvMytextview.text = timesClicked.toString()

        }

        btn3Clickme.setOnClickListener {
            tvMySave.text = timesClicked.toString()
        }
    }
}
