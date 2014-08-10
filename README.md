ali
===
using UnityEngine;
using System.Collections;

public class GamePlay : MonoBehaviour {
	public int slice = 0;
	public Transform player; // Drag your player here
	private Vector2 fp; // first finger position
	private Vector2 lp; // last finger position
	public Score Score;
	public bool Firsttime = false;
	public AudioClip Sound;
	public AudioClip Sound1;
	public Tut Tut;
	public bool IsCreated = false;
	public int pola = 0;
	public bool Start = false;
	public bool left1 = false;
	public bool right1 = false;
	public bool up1 = false;
	public bool down1 = false;
	public bool touch1 = false;
	public Level1 Level1;


	

	void Update () {

		int randomPick = Mathf.Abs(Random.Range(1,40));

		foreach(Touch touch in Input.touches)
		{
			if (touch.phase == TouchPhase.Began)
			{
				fp = touch.position;
				lp = touch.position;
			}
			if (touch.phase == TouchPhase.Moved )
			{
				lp = touch.position;
			}
			if(touch.phase == TouchPhase.Ended)
			{

				if(((fp.x - lp.x) > 80)  && (slice == 1) && (pola == 1) && (GameObject.Find("P-Slice1"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice1"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 2) && (pola == 2) && (GameObject.Find("P-Slice2"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice2"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 3) && (pola == 3) && (GameObject.Find("P-Slice3"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice3"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 4) && (pola == 4) && (GameObject.Find("P-Slice4"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice4"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 5) && (pola == 5) && (GameObject.Find("P-Slice5"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice5"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 6) && (pola == 6) && (GameObject.Find("P-Slice6"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice6"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 7) && (pola == 7) && (GameObject.Find("P-Slice7"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice7"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
				}
				else if(((fp.x - lp.x) > 80)  && (slice == 8) && (pola == 8) && (GameObject.Find("P-Slice8"))) // left swipe
				{
					Destroy (GameObject.Find("P-Slice8"));
					Score.score += 100;
					Firsttime = true;
					audio.PlayOneShot(Sound);
					audio.PlayOneShot(Sound1);
					Level1.play += 1;
				}
				else if(((fp.x - lp.x) < -80) && (slice == 9) && (pola == 9) && (GameObject.Find("P-Slice1"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice1"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 10) && (pola == 10) && (GameObject.Find("P-Slice2"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice2"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 11) && (pola == 11) && (GameObject.Find("P-Slice3"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice3"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 12) && (pola == 12) && (GameObject.Find("P-Slice4"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice4"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 13) && (pola == 13) && (GameObject.Find("P-Slice5"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice5"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 14) && (pola == 14) && (GameObject.Find("P-Slice6"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice6"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 15) && (pola == 15) && (GameObject.Find("P-Slice7"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice7"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.x - lp.x) < -80) && (slice == 16) && (pola == 16) && (GameObject.Find("P-Slice8"))) // right swipe
				{
					Destroy (GameObject.Find("P-Slice8"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
					Level1.play += 1;
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 17) && (pola == 17) && (GameObject.Find("P-Slice1"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice1"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 18) && (pola == 18) && (GameObject.Find("P-Slice2"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice2"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 19) && (pola == 19) && (GameObject.Find("P-Slice3"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice3"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 20) && (pola == 20) && (GameObject.Find("P-Slice4"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice4"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 21) && (pola == 21) && (GameObject.Find("P-Slice5"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice5"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 22) && (pola == 22) && (GameObject.Find("P-Slice6"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice6"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 23) && (pola == 23) && (GameObject.Find("P-Slice7"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice7"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) < -80)  && (slice == 24) && (pola == 24) && (GameObject.Find("P-Slice8"))) // up swipe
				{
					Destroy (GameObject.Find("P-Slice8"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
					Level1.play += 1;
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 25) && (pola == 25) && (GameObject.Find("P-Slice1"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice1"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 26) && (pola == 26) && (GameObject.Find("P-Slice2"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice2"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 27) && (pola == 27) && (GameObject.Find("P-Slice3"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice3"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 28) && (pola == 28) && (GameObject.Find("P-Slice4"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice4"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 29) && (pola == 29) && (GameObject.Find("P-Slice5"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice5"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 30) && (pola == 30) && (GameObject.Find("P-Slice6"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice6"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 31) && (pola == 31) && (GameObject.Find("P-Slice7"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice7"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if(((fp.y - lp.y) > 80)  && (slice == 32) && (pola == 32) && (GameObject.Find("P-Slice8"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice8"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
					Level1.play += 1;
				}
				else if ((Input.GetMouseButtonDown(0)) && (slice == 33) && (pola == 33) && (GameObject.Find("P-Slice1"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice1"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0)) && (slice == 34) && (pola == 34) && (GameObject.Find("P-Slice2"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice2"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0)) && (slice == 35) && (pola == 35) && (GameObject.Find("P-Slice3"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice3"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0)) && (slice == 36) && (pola == 36) && (GameObject.Find("P-Slice4"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice4"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0)) && (slice == 37) && (pola == 37) && (GameObject.Find("P-Slice5"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice5"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0))  && (slice == 38) && (pola == 38) && (GameObject.Find("P-Slice6"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice6"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0))  && (slice == 39) && (pola == 39) && (GameObject.Find("P-Slice7"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice7"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
				}
				else if ((Input.GetMouseButtonDown(0))  && (slice == 40) && (pola == 40) && (GameObject.Find("P-Slice8"))) // down swipe
				{
					Destroy (GameObject.Find("P-Slice8"));
					Score.score += 100;
					audio.PlayOneShot(Sound);
					Level1.play += 1;
				}
			if((randomPick == 1) && (GameObject.Find("P-Slice1"))){
				slice = 1;
				pola = 1;
				left1 = true;
			}
			if((randomPick == 2) && (GameObject.Find("P-Slice2"))){
				slice = 2;
				pola = 2;
				left1 = true;
			}
			if((randomPick == 3) && (GameObject.Find("P-Slice3"))){
				slice = 3;
				pola = 3;
				left1 = true;
			}
			if((randomPick == 4) && (GameObject.Find("P-Slice4"))){
				slice = 4;
				pola = 4;
				left1 = true;
			}
			if((randomPick == 5) && (GameObject.Find("P-Slice5"))){
				slice = 5;
				pola = 5;
				left1 = true;
			}
			if((randomPick == 6) && (GameObject.Find("P-Slice6"))){
				slice = 6;
				pola = 6;
				left1 = true;
			}
			if((randomPick == 7) && (GameObject.Find("P-Slice7"))){
				slice = 7;
				pola = 7;
				left1 = true;
			}
			if((randomPick == 8) && (GameObject.Find("P-Slice8"))){
				slice = 8;
				pola = 8;
				left1 = true;
			}
			if((randomPick == 9) && (GameObject.Find("P-Slice1"))){
				slice = 9;
				pola = 9;
				right1 = true;
			}
			if((randomPick == 10) && (GameObject.Find("P-Slice2"))){
				slice = 10;
				pola = 10;
				right1 = true;
				}
			if((randomPick == 11) && (GameObject.Find("P-Slice3"))){
				slice = 11;
				pola = 11;
				right1 = true;
				}
			if((randomPick == 12) && (GameObject.Find("P-Slice4"))){
				slice = 12;
				pola = 12;
				right1 = true;
				}
			if((randomPick == 13) && (GameObject.Find("P-Slice5"))){
				slice = 13;
				pola = 13;
				right1 = true;
				}
			if((randomPick == 14) && (GameObject.Find("P-Slice6"))){
				slice = 14;
				pola = 14;
				right1 = true;
				}
			if((randomPick == 15) && (GameObject.Find("P-Slice7"))){
				slice = 15;
				pola = 15;
				right1 = true;
				}
			if((randomPick == 16) && (GameObject.Find("P-Slice8"))){
				slice = 16;
				pola = 16;
				right1 = true;
				}
			if((randomPick == 17) && (GameObject.Find("P-Slice1"))){
				slice = 17;
				pola = 17;
				up1 = true;	
				}
			if((randomPick == 18) && (GameObject.Find("P-Slice2"))){
				slice = 18;
				pola = 18;
				up1 = true;	
				}
			if((randomPick == 19) && (GameObject.Find("P-Slice3"))){
				slice = 19;
				pola = 19;
				up1 = true;	
				}
			if((randomPick == 20) && (GameObject.Find("P-Slice4"))){
				slice = 20;
				pola = 20;
				up1 = true;	
				}
			if((randomPick == 21) && (GameObject.Find("P-Slice5"))){
				slice = 21;
				pola = 21;
				up1 = true;	
				}
			if((randomPick == 22) && (GameObject.Find("P-Slice6"))){
				slice = 22;
				pola = 22;
				up1 = true;	
				}
			if((randomPick == 23) && (GameObject.Find("P-Slice7"))){
				slice = 23;
				pola = 23;
				up1 = true;	
				}
			if((randomPick == 24) && (GameObject.Find("P-Slice8"))){
				slice = 24;
				pola = 24;
				up1 = true;	
				}
			if((randomPick == 25) && (GameObject.Find("P-Slice1"))){
				slice = 25;
				pola = 25;
				down1 = true;	
				}
			if((randomPick == 26) && (GameObject.Find("P-Slice2"))){
				slice = 26;
				pola = 26;
				down1 = true;	
				}
			if((randomPick == 27) && (GameObject.Find("P-Slice3"))){
				slice = 27;
				pola = 27;
				down1 = true;	
				}
			if((randomPick == 28) && (GameObject.Find("P-Slice4"))){
				slice = 28;
				pola = 28;
				down1 = true;	
				}
			if((randomPick == 29) && (GameObject.Find("P-Slice5"))){
				slice = 29;
				pola = 29;
				down1 = true;	
				}
			if((randomPick == 30) && (GameObject.Find("P-Slice6"))){
				slice = 30;
				pola = 30;
				down1 = true;	
				}
			if((randomPick == 31) && (GameObject.Find("P-Slice7"))){
				slice = 31;
				pola = 31;
				down1 = true;	
				}
			if((randomPick == 32) && (GameObject.Find("P-Slice8"))){
				slice = 32;
				pola = 32;
				down1 = true;	
				}
			if((randomPick == 33) && (GameObject.Find("P-Slice1"))){
					slice = 33;
					pola = 33;
					touch1 = true;	
				}
			if((randomPick == 34) && (GameObject.Find("P-Slice2"))){
					slice = 34;
					pola = 34;
					touch1 = true;	
				}
			if((randomPick == 35) && (GameObject.Find("P-Slice3"))){
					slice = 35;
					pola = 35;
					touch1 = true;	
				}
			if((randomPick == 36) && (GameObject.Find("P-Slice4"))){
					slice = 36;
					pola = 36;
					touch1 = true;	
				}
			if((randomPick == 37) && (GameObject.Find("P-Slice5"))){
					slice = 37;
					pola = 37;
					touch1 = true;	
				}
			if((randomPick == 38) && (GameObject.Find("P-Slice6"))){
					slice = 38;
					pola = 38;
					touch1 = true;	
				}
			if((randomPick == 39) && (GameObject.Find("P-Slice7"))){
					slice = 39;
					pola = 39;
					touch1 = true;	
				}
			if((randomPick == 40) && (GameObject.Find("P-Slice8"))){
					slice = 40;
					pola = 40;
					touch1 = true;	
				}
				if ((left1 == true)){
					Destroy (GameObject.Find("Arrow-R(Clone)"));
					Destroy (GameObject.Find("Arrow-L(Clone)"));
					Destroy (GameObject.Find("Arrow-U(Clone)"));
					Destroy (GameObject.Find("Arrow-D(Clone)"));
					Destroy (GameObject.Find("Touch(Clone)"));
					Instantiate(Resources.Load("Arrow-L"), new Vector3(0.85f,0.85f,0.85f), Quaternion.identity);
					left1 = false;
				}
				if ((right1 == true)){
					Destroy (GameObject.Find("Arrow-R(Clone)"));
					Destroy (GameObject.Find("Arrow-L(Clone)"));
					Destroy (GameObject.Find("Arrow-U(Clone)"));
					Destroy (GameObject.Find("Arrow-D(Clone)"));
					Destroy (GameObject.Find("Touch(Clone)"));
					Instantiate(Resources.Load("Arrow-R"), new Vector3(0.85f,0.85f,0.85f), Quaternion.identity);
					right1 = false;
				}
				if ((up1 == true)){
					Destroy (GameObject.Find("Arrow-R(Clone)"));
					Destroy (GameObject.Find("Arrow-L(Clone)"));
					Destroy (GameObject.Find("Arrow-U(Clone)"));
					Destroy (GameObject.Find("Arrow-D(Clone)"));
					Destroy (GameObject.Find("Touch(Clone)"));
					Instantiate(Resources.Load("Arrow-U"), new Vector3(0.85f,0.85f,0.85f), Quaternion.identity);
					up1 = false;
				}
				if ((down1 == true)){
					Destroy (GameObject.Find("Arrow-R(Clone)"));
					Destroy (GameObject.Find("Arrow-L(Clone)"));
					Destroy (GameObject.Find("Arrow-U(Clone)"));
					Destroy (GameObject.Find("Arrow-D(Clone)"));
					Destroy (GameObject.Find("Touch(Clone)"));
					Instantiate(Resources.Load("Arrow-D"), new Vector3(0.85f,0.85f,0.85f), Quaternion.identity);
					down1 = false;
				}
				if ((touch1 == true)){
					Destroy (GameObject.Find("Arrow-R(Clone)"));
					Destroy (GameObject.Find("Arrow-L(Clone)"));
					Destroy (GameObject.Find("Arrow-U(Clone)"));
					Destroy (GameObject.Find("Arrow-D(Clone)"));
					Destroy (GameObject.Find("Touch(Clone)"));
					Instantiate(Resources.Load("Touch"), new Vector3(0.85f,0.85f,0.85f), Quaternion.identity);
					touch1 = false;
				}
		}
	}
}
}
