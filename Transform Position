using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class backnforth : MonoBehaviour
{
    public Transform Plat1, Plat2;
    public float speed;
    public Transform startPos;

    Vector3 nextPos;

    void Start()
    {
        nextPos = startPos.position;
    }

    void FixedUpdate()
    {
        if(transform.position==Plat1.position)
        {
            nextPos=Plat2.position;
        }
        if (transform.position == Plat2.position)
        {
            nextPos = Plat1.position;

        }
        transform.position = Vector3.MoveTowards(transform.position, nextPos, speed * Time.deltaTime);
    }
    private void OnDrawGizmos()
    {
        Gizmos.DrawLine(Plat1.position, Plat2.position);
    }
}

