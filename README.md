# My-Portfolio

1. Clone the project from https://github.com/kush-raj-nit061/My-Portfolio

2. Change constraint layout in mainactivity.xml file to ScrollView

# Creating the Layout

To arrange all the layouts and views Vertically

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">
    </LinearLayout>

To arrange the Views present at top of portfolio app

    <RelativeLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"> 
    </RelativeLayout>

All the views that will be present at top

            <Toolbar
                android:layout_width="match_parent"
                android:background="#C0C0C0"
                android:layout_height="90dp"/>
            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:textSize="35sp"
                android:layout_alignParentBottom="true"
                android:layout_centerHorizontal="true"
                android:textColor="@color/black"
                android:textAllCaps="true"
                android:text="My Portfolio"
                android:textStyle="bold"
                android:fontFamily="@font/roboto_bold"/>
            <ImageView
                android:id="@+id/edit"
                android:layout_width="35dp"
                android:layout_height="35dp"
                android:layout_marginTop="45dp"
                android:layout_alignParentEnd="true"
                android:layout_marginEnd="10dp"
                android:src="@drawable/edit"/>

1:1 image present on top working like a background image

        <androidx.constraintlayout.widget.ConstraintLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <ImageView
                android:id="@+id/image_view"
                android:layout_width="0dp"
                android:layout_height="0dp"
                android:adjustViewBounds="true"
                android:src="@drawable/pic"
                app:layout_constraintDimensionRatio="1:1"
                app:layout_constraintStart_toStartOf="parent"
                app:layout_constraintEnd_toEndOf="parent"
                app:layout_constraintTop_toTopOf="parent"
                app:layout_constraintBottom_toBottomOf="parent" />

            
        </androidx.constraintlayout.widget.ConstraintLayout>

To create a gradient effect from bottom to top

            <TextView
                android:layout_width="match_parent"
                android:layout_height="0dp"
                android:alpha="0.6"
                android:background="@drawable/gradient"
                app:layout_constraintBottom_toBottomOf="@+id/image_view"
                app:layout_constraintTop_toTopOf="parent" />


Creating a layout bottom profile section

            <RelativeLayout
                android:layout_width="match_parent"
                android:layout_height="200dp"
                app:layout_constraintBottom_toBottomOf="parent"
                android:paddingHorizontal="8dp"
                android:paddingBottom="2dp"
                android:gravity="bottom"
                android:background="@drawable/gradient_white"
                app:layout_constraintEnd_toEndOf="parent"
                app:layout_constraintStart_toStartOf="parent">

            </RelativeLayout>


Creating a layout for holding Profile image

                <androidx.constraintlayout.widget.ConstraintLayout
                    android:id="@+id/constraint"
                    android:layout_width="100dp"
                    android:layout_height="100dp"
                    android:background="@drawable/card_stroke"
                    >
                    <ImageView
                        android:id="@+id/profile"
                        android:layout_width="0dp"
                        android:layout_height="0dp"
                        android:padding="5dp"
                        android:src="@drawable/pic"
                        android:adjustViewBounds="true"
                        android:scaleType="centerCrop"
                        app:layout_constraintDimensionRatio="1:1"
                        app:layout_constraintStart_toStartOf="parent"
                        app:layout_constraintEnd_toEndOf="parent"
                        app:layout_constraintTop_toTopOf="parent"
                        app:layout_constraintBottom_toBottomOf="parent" />


                </androidx.constraintlayout.widget.ConstraintLayout>


Creating a layout for holding name and speciality

                <LinearLayout
                    android:layout_width="wrap_content"
                    android:orientation="vertical"
                    android:layout_toEndOf="@id/constraint"
                    android:layout_height="wrap_content">

                    
                </LinearLayout>

Adding views of firstname, lastname and speciality


                    <TextView
                        android:id="@+id/first_name"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:layout_marginStart="12dp"
                        android:layout_marginTop="8dp"
                        android:layout_marginBottom="4dp"
                        android:layout_toEndOf="@id/constraint"
                        android:fontFamily="@font/roboto_bold"
                        android:text="Ananya"
                        android:textColor="@color/black"
                        android:textSize="20sp"
                        android:textStyle="bold" />

                    <TextView
                        android:id="@+id/last_name"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:layout_marginStart="12dp"
                        android:layout_marginTop="-5dp"
                        android:layout_marginBottom="4dp"
                        android:layout_toEndOf="@id/constraint"
                        android:fontFamily="@font/roboto_bold"
                        android:text="Pandey"
                        android:textColor="@color/black"
                        android:textSize="20sp"
                        android:textStyle="bold" />
                    <TextView
                        android:id="@+id/speciality"
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:text="Maine bhot struggle kiya hai"
                        android:textColor="@color/black"
                        android:textSize="14sp"
                        android:textStyle="bold"
                        android:layout_toEndOf="@id/constraint"
                        android:fontFamily="@font/museo"
                        android:layout_marginTop="4dp"
                        android:layout_marginStart="12dp"
                        android:layout_marginBottom="4dp"
                        />

        
Adding views for about

        <TextView
            android:id="@+id/about"
            android:layout_marginHorizontal="8dp"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:alpha="1"
            android:fontFamily="@font/museo"
            android:text=" || 10th pass || 12th pass || Btech || Mtech || PhD ||"
            android:textColor="@color/black" />


Adding views for Achievement

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Achievements"
            android:layout_marginTop="20dp"
            android:layout_marginStart="8dp"
            android:textStyle="bold"
            android:textColor="@color/black"
            android:fontFamily="@font/museo"
            android:textSize="16sp"/>

        <androidx.recyclerview.widget.RecyclerView
            android:id="@+id/rec"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:layoutManager="androidx.recyclerview.widget.LinearLayoutManager"
            android:orientation="horizontal"
            android:layout_marginTop="8dp"/>


#layout for item

        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            app:cardCornerRadius="8dp">
            <androidx.constraintlayout.widget.ConstraintLayout
                android:layout_width="match_parent"
                android:layout_height="match_parent">

                <ImageView
                    android:id="@+id/postImage"
                    android:layout_width="0dp"
                    android:layout_height="0dp"
                    android:scaleType="fitXY"
                    app:layout_constraintDimensionRatio="4:3"
                    app:layout_constraintBottom_toBottomOf="parent"
                    app:layout_constraintEnd_toEndOf="parent"
                    app:layout_constraintStart_toStartOf="parent" />

            </androidx.constraintlayout.widget.ConstraintLayout>
        </androidx.cardview.widget.CardView>
        <androidx.constraintlayout.widget.ConstraintLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <TextView
                android:id="@+id/event_heading"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Silver"
                android:layout_marginStart="5dp"
                android:layout_marginTop="5dp"
                app:layout_constraintTop_toTopOf="parent"
                app:layout_constraintStart_toStartOf="parent"
                android:textColor="@color/black"
                android:fontFamily="@font/roboto_bold"/>

            <TextView
                android:id="@+id/event_name"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Innovolt 2021"
                android:textColor="#393636"
                app:layout_constraintTop_toBottomOf="@id/event_heading"
                app:layout_constraintStart_toStartOf="parent"
                android:layout_marginStart="5dp"
                android:layout_marginTop="-2dp"
                android:fontFamily="@font/roboto"/>

            <ImageView
                android:id="@+id/info"
                android:layout_width="20dp"
                android:layout_height="20dp"
                android:layout_marginEnd="16dp"
                app:layout_constraintBottom_toBottomOf="parent"
                android:src="@drawable/info"
                app:layout_constraintEnd_toEndOf="parent"
                app:layout_constraintTop_toTopOf="parent" />


        </androidx.constraintlayout.widget.ConstraintLayout>
        <androidx.cardview.widget.CardView
            android:layout_width="match_parent"
            android:layout_height="30dp"
            app:cardBackgroundColor="#C0C0C0"
            app:cardCornerRadius="5dp">

            <LinearLayout
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:orientation="horizontal">
                <LinearLayout
                    android:layout_width="wrap_content"
                    android:layout_height="match_parent"
                    android:layout_weight="0.3"
                    android:orientation="vertical">
                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:text="Date:"
                        android:paddingStart="4dp"
                        android:textColor="@color/black"
                        android:textSize="12sp"/>
                    <TextView
                        android:id="@+id/date"
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:textSize="10sp"
                        android:textStyle="bold"
                        android:paddingStart="4sp"
                        android:textColor="#FFFFFF"
                        android:text=""/>


                </LinearLayout>

                

                <LinearLayout
                    android:layout_width="wrap_content"
                    android:layout_height="match_parent"
                    android:layout_weight="0.5"
                    android:orientation="vertical">
                    <TextView
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:text="Place:"
                        android:textAlignment="center"
                        android:textColor="@color/black"
                        android:textSize="12sp"/>
                    <TextView
                        android:id="@+id/venue"
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:singleLine="true"
                        android:focusable="true"
                        android:ellipsize="marquee"
                        android:marqueeRepeatLimit="marquee_forever"
                        android:fontFamily="@font/roboto"
                        android:focusableInTouchMode="true"
                        android:maxWidth="40dp"
                        android:textSize="10sp"
                        android:textStyle="bold"
                        android:textAlignment="center"
                        android:textColor="#FFFFFF"
                        android:text=""/>


                </LinearLayout>

            </LinearLayout>
        </androidx.cardview.widget.CardView>


# Backend Integration

Creating objects of all the views whose value needs to be changed

    private lateinit var rec:RecyclerView
    private lateinit var firstName:TextView
    private lateinit var lastName:TextView
    private lateinit var speciality:TextView
    private lateinit var about:TextView
    private lateinit var theme_image:ImageView
    private lateinit var profile:ImageView
    private var data:String =""

Linking views with their respective ids

        rec = findViewById(R.id.rec)
        firstName = findViewById(R.id.first_name)
        lastName = findViewById(R.id.last_name)
        speciality = findViewById(R.id.speciality)
        about = findViewById(R.id.about)
        theme_image = findViewById(R.id.image_view)
        profile = findViewById(R.id.profile)
        rec.itemAnimator=  null

Making object to receive values from realtime database

    private val dbRef = FirebaseDatabase.getInstance().reference

Receiving values from realtime database

        dbRef.child("MyProfile").addListenerForSingleValueEvent(object :ValueEventListener{
            override fun onDataChange(snapshot: DataSnapshot) {
                if(snapshot.exists()){
                    firstName.text = snapshot.child("first_name").value.toString()
                    lastName.text = snapshot.child("last_name").value.toString()
                    speciality.text = snapshot.child("speciality").value.toString()
                    data = snapshot.child("about").value.toString()
                    Glide.with(applicationContext).load(snapshot.child("theme_image").value.toString()).into(theme_image)
                    Glide.with(applicationContext).load(snapshot.child("profile").value.toString()).into(profile)
                    val anotherReadMore: AnotherReadMore = AnotherReadMore.Builder()
                        .moreLabel("more")
                        .lessLabel("less")
                        .build()

                    anotherReadMore.addReadMoreTo(about, data)
                }
            }

            override fun onCancelled(error: DatabaseError) {
                TODO("Not yet implemented")
            }

        })

Making object for one item of Recycler view with adapter

    private lateinit var achievementAdapter: AchievementAdapter


Linking adapter and recycler view with firebase

        val options: FirebaseRecyclerOptions<AchievementData?> =
            FirebaseRecyclerOptions.Builder<AchievementData>()
                .setQuery(
                    FirebaseDatabase.getInstance().reference.child("MyProfile").child("Achievement"),
                    AchievementData::class.java
                )
                .build()
        achievementAdapter = AchievementAdapter(options)

        rec.adapter = achievementAdapter
        achievementAdapter.startListening()



# Writing codes for adapter

Creating objects for all views of item

        var posterImage:ImageView
        var event_name:TextView
        var event_heading:TextView
        var date:TextView
        var venue:TextView


Assigning id's of all objects

            posterImage =innerView.findViewById(R.id.postImage)
            event_name = innerView.findViewById(R.id.event_name)
            event_heading = innerView.findViewById(R.id.event_heading)
            date = innerView.findViewById(R.id.date)
            venue = itemView.findViewById(R.id.venue)

Assignig data to each objects

        holder.event_name.text = model.event_name
        holder.event_heading.text = model.event_heading
        holder.date.text = model.event_date
        holder.venue.text = model.event_venue
        Glide.with(holder.posterImage.context).load(model.posterImage).into(holder.posterImage)
